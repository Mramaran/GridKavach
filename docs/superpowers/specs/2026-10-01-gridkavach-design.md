# GridKavach: Concept Design

**Date:** 2026-10-01
**Hackathon:** Schneider Electric Yuva Yodha Energy Tech Hackathon 2026, submission deadline 2026-10-04
**Challenge:** 03 Grid Reliability ("Renewable Intermittency")
**Status:** Concept approved; this document is the single source for the application text and the deck.

> Items marked **[verify]** must be checked against a citable source before submission. Items marked **[assume]** are model inputs to be stated openly as assumptions.

---

## 1. One-liner

**GridKavach keeps a neighbourhood's power dependable when solar falls short, and keeps people safe on a grid full of rooftop solar, batteries and inverters.**

Tagline: *Forecast the gap. Share the battery. Protect the essentials. Shield the line.*

## 2. Alignment with Challenge 03

| Challenge 03 goal or deliverable | How GridKavach meets it |
|---|---|
| Bridge intermittency gaps | Gap Radar forecasts the shortfall; the shared battery and load shifting cover it; essential-tier rationing covers what's left |
| Local and manageable | Runs per feeder or neighbourhood on one edge server; operated locally by an RWA or SHG operator |
| Affordable for low-income urban/peri-urban | One shared battery instead of a private inverter in every home; a small monthly household fee for guaranteed essential power |
| Support the DISCOM | Feeder-stress forecasts, a demand-response capacity signal, fault location (LastGasp), safe work permits (SafeLine) |
| Measurable reliability vs baseline | Essential-supply availability during intermittency windows, plus outage customer-minutes, vs today's load shedding |
| Ownership, O&M, unit economics | §8 |
| Architecture diagram with data, energy and money flows | §5 |
| Prototype or simulation | The existing `scada` codebase, extended (§6) |

The challenge's own "ideas to get you started" that we cover: shared storage with fair-access and dispatch rules; microgrid control with critical-load prioritisation; forecasting and load-shifting tools; DISCOM analytics for feeder stress.

## 3. Problem: hero setting

**Setting:** a dense, low-income urban neighbourhood, such as a resettlement colony or chawl cluster, of roughly 300–500 households plus small shops, a clinic and a school, on one LT/11 kV feeder segment. **[assume size]**

1. **The evening gap.** Solar output collapses after sunset just as household demand peaks. When supply is short, the DISCOM's only tool is rotating load shedding, and the whole neighbourhood goes dark: no study light, no fan in a heatwave, no fridge for medicines, no small business.
2. **Backup is unequal.** Better-off homes buy private inverters, and poorer homes can't. Those private inverters are many small, uncoordinated batteries.
3. **More sources, more danger.** Rooftop solar, home inverters and DG sets can feed power back into a line the crew believes is dead **[verify accident statistics]**. Faults on underground cable are found by trial-and-error switching. When power returns after a long outage, the cold-load surge can re-trip the feeder.

Why now: India's renewable build-out to 2047 and the smart-meter rollout under RDSS **[verify]** make both the problem and the solution timely.

## 4. Solution: three layers

### Layer 1: Gap Radar (forecast)
- Forecasts solar output, load and battery state 24 hours ahead per feeder, and computes the **intermittency gap** (demand minus local renewables minus available grid allocation) hour by hour.
- Publishes a **feeder-stress forecast** and the neighbourhood's **flexible capacity** (kW that can be shifted or curtailed) to the DISCOM.

### Layer 2: Flex (headline): shared battery and essential-load priority
1. **Shift:** nudges via SMS or WhatsApp in the local language move flexible loads (washing, water pumping, e-rickshaw charging) into solar hours. Smart plugs or meters can be scheduled where available.
2. **Share:** one community battery (second-life batteries allowed) charges on midday surplus and discharges into the forecast gap. Dispatch rules are fair-access: each household gets an equal essential-energy allowance.
3. **Protect essentials:** if a gap remains, smart-meter load limits drop each home to an **essential tier** (lights, fan, phone charging, medical devices) instead of a full blackout. Clinic and school are always tier 0.
   - Tier 0: critical facilities · Tier 1: household essentials (~100–200 W per home **[assume]**) · Tier 2: fridge and TV · Tier 3: AC, geyser, pumps.

### Layer 3: Kavach (protection)
- **LastGasp:** smart-meter power-fail events are mapped onto feeder topology to locate the faulted section, isolate it, and restore the healthy sections through an alternate feed. **[verify meter last-gasp support, e.g. IS 16444]**
- **SafeLine:** a digital permit-to-work. Before a section is handed to a crew, the SCADA finds all back-feed sources on it (community battery, rooftop PV, home inverters, DG sets), commands them to stop exporting, verifies zero voltage, and requires double confirmation (JE approves, lineman or jointer acknowledges). The section is locked until the permit is returned.
- **ColdStart:** predicts the cold-load surge from outage duration and season, then re-energises in waves with community-battery support so the feeder does not re-trip.

**Why Kavach belongs in an intermittency solution:** every flexibility tool the challenge suggests adds distributed sources and storage to the feeder. GridKavach is the one that makes that safe and recoverable.

## 5. Architecture

```
                 ┌──────────── DISCOM control room ────────────┐
                 │  feeder-stress forecast · DR capacity · fault │
                 │  location · permit approvals (JE/SDO roles)   │
                 └──────────────▲───────────────┬───────────────┘
                     data (REST/WS)│               │ DR signal, permit approval
┌────────────────────────── GridKavach feeder server ──────────────────────────┐
│ Gap Radar (forecasts) │ Flex engine (battery dispatch, tiers) │ Kavach        │
│                       │                                       │ (LastGasp,    │
│        feeder topology model: sections, RMUs, breakers, meters│  SafeLine,    │
│                                                               │  ColdStart)   │
└───────▲──────────────────────▲───────────────────────▲────────────────────────┘
        │ Modbus/IEC 61850     │ meter events/limits   │ SMS/WhatsApp nudges
┌───────┴────────┐   ┌─────────┴──────────┐   ┌────────┴─────────┐
│ Community      │   │ Smart meters       │   │ Households,      │
│ battery + PV   │   │ (each home)        │   │ shops, clinic    │
│ (existing EMS) │   └────────────────────┘   └──────────────────┘
└────────────────┘
```

**Flows (draw all three on the diagram slide):**
- **Energy:** grid + rooftop/community PV → community battery → feeder → homes (tiered during gaps).
- **Data:** meters and inverters → GridKavach → DISCOM forecasts and DR signal; DISCOM → DR requests and permit approvals.
- **Money:** households → local operator (monthly essential-power fee); DISCOM → operator (DR payments) and → GridKavach (per-feeder licence); solar installers → GridKavach (inverter registry fee).

## 6. Built on the existing codebase

The working code is in `github.com/veneshvpm/scada` (~11k lines). **`scadaheck` currently has only a README: push the code there or link `scada` before submitting.**

| Existing (`scada`) | Becomes |
|---|---|
| `ems.py` 4 dispatch modes + Q-learning battery scheduler | Community battery dispatch; reward gets a fair-access term and a restoration-reserve term |
| `ai_models.py` load, solar and wind forecasters | Gap Radar |
| `ai_models.py` AnomalyDetector | Voltage on a section that should be de-energised (SafeLine) |
| Grid-outage detection → islanding (`ems.py`) | Back-feed source detection |
| `protocols.py` Modbus 40005 export-enable | SafeLine interlock command |
| `protocols.py` IEC 61850 `XCBR.Pos` | Section breaker status and switching |
| `/api/twin/simulate-failure` | Demo trigger (cable fault, evening solar drop) |
| Alarms ack/clear/repair + JWT RBAC | Permit lifecycle; roles: household, local operator, lineman/jointer, JE, DISCOM |
| Troubleshooting SOPs in `ems.py` | Permit isolation checklist |
| `/api/carbon-analytics` | Diesel avoided (DG sets displaced) |

**New work:**
1. Feeder topology model (sections, RMUs, breakers, meters, sources)
2. Smart-meter simulator: per-home load, tier limits, power-fail events
3. Gap computation + tier rationing in the EMS loop
4. LastGasp localisation algorithm
5. SafeLine permit state machine and section lock
6. ColdStart wave planner
7. UI: feeder view on the SLD, permit screen, DISCOM panel, household view (mock SMS)
8. Baseline-vs-GridKavach simulation runner (§7)

## 7. Measuring impact (simulation, against a defined baseline)

**Baseline:** today's practice. During an intermittency gap the DISCOM rotates load shedding (whole sections off); faults are located by sequential RMU switching; restoration energises everything at once; no back-feed check.

**Method:** run N simulated days (e.g. 30 days of seeded data plus evening-gap and fault scenarios) under the baseline and under GridKavach, with the same inputs.

| Metric | Definition | Challenge link |
|---|---|---|
| **Essential-supply availability (headline)** | % of intermittency-window hours in which each home has at least tier-1 power | "increased supply availability during intermittency windows" |
| Household outage hours | Hours with zero supply per household per month | "reduction in outage hours" |
| Local renewable utilisation | % of local PV used locally instead of curtailed | Bridge gaps |
| Peak feeder load during gap | kW drawn from the DISCOM in the evening peak | Support DISCOM |
| Fault location time | Minutes, LastGasp vs sequential switching | Reliability |
| Back-feed exposures | Exporting sources on a permitted section (target: 0) | Safety |
| Re-trips on restoration | Count, ColdStart vs simultaneous energisation | Reliability |

Report only numbers the simulator produces, and state the assumptions.

## 8. Ownership, operations, unit economics

- **Owner and operator:** a neighbourhood RWA or women's SHG cooperative owns the community battery and employs one trained local operator, who uses the operator role in the app.
- **Maintenance:** battery and inverter O&M under an installer AMC; GridKavach software maintained by us, remote updates.
- **DISCOM role:** grid connection, DR programme, permit approvals; licenses GridKavach per feeder.

**Unit economics template** (fill with sourced or assumed values):

| Item | Formula | Input |
|---|---|---|
| Battery size | households × tier-1 W × gap hours ÷ depth of discharge | [assume] |
| Capex | battery kWh × ₹/kWh (second-life cheaper) + inverter + meters/plugs | [verify prices] |
| Annual cost | capex ÷ life (yrs) + O&M + operator wage + licence | [assume] |
| Revenue | household fee × households × 12 + DR payments + evening arbitrage | [assume DR rate] |
| **Affordability test** | household fee vs cost of a private inverter or kerosene/candles | [verify] |

The pitch claim to prove: *essential power for every home for less than a private inverter costs one home*.

## 9. Business model

- **Core:** DISCOM per-feeder licence, sold as an add-on to the smart-meter rollout.
- **Growth:** installer fee per inverter in the SafeLine back-feed registry (tied to net-metering approval).
- **Scale:** low-voltage module for Schneider's grid-management (ADMS / EcoStruxure Grid) channel.

## 10. Roadmap

1. **Now:** simulation prototype on `scada`.
2. **Pilot:** one low-income urban feeder with a DISCOM + RWA/SHG.
3. **Expand:** peri-urban feeders (more pole work → SafeLine), rural agricultural feeders (long lines → LastGasp, pump shifting).
4. **Scale:** Schneider integration; state-level rollout aligned with the smart-meter rollout.

## 11. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Inverters not remotely controllable | SafeLine falls back to detect-and-block-permit |
| Meters lack last-gasp events | Use communication-loss patterns from the smart-meter head-end |
| Tier rationing seen as unfair | Equal essential allowance, transparent rules, operator override with audit log |
| Data or connectivity outages | Edge server runs autonomously; SMS fallback |
| Cybersecurity of remote load control | RBAC, double confirmation, audit trail (existing) |

## 12. Demo storyline (3 minutes)

1. **6:30 pm, clouds + sunset:** Gap Radar showed a 40-minute gap at 3 pm; nudges went out; the battery was pre-charged.
2. **7:15 pm, gap hits:** the battery covers most of it; the remainder triggers tier-1 rationing. Every home keeps lights and fans; the clinic stays at full power. Baseline view: whole section dark.
3. **7:42 pm, cable fault:** LastGasp locates the section; healthy sections are restored via the alternate feed.
4. **Permit:** SafeLine finds a home inverter and the community battery exporting; commands them off; zero voltage verified; JE + jointer confirm; section locked.
5. **Restore:** ColdStart brings the section back in three waves; no re-trip.
6. **Scoreboard:** baseline vs GridKavach metrics (§7).
