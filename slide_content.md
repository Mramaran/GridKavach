# GridKavach: Slide Content for Canva

**Deck:** 12 slides, 16:9 · Schneider Electric Yuva Yodha Energy Tech Hackathon 2026 · Challenge 03 Grid Reliability

---

## Design brief (paste this into Canva first)

- **Theme:** Schneider-inspired green. Clean white slides with a bold green title band or left accent bar. Title and closing slides are full dark green with white text.
- **Colours:**
  - Primary green `#3DCD58` (accent bars, icons, highlights, "GridKavach" numbers)
  - Dark green `#009530` (title-slide background, headings)
  - Charcoal `#333333` (body text)
  - Light grey `#F4F6F8` (panels and cards)
  - Blue `#2F80ED` (data arrows only)
  - Amber `#F2A900` (money arrows, TARGET / assumption labels)
  - Red `#E5484D` (danger and baseline only)
- **Branding rule:** use Schneider-style *colours* only. **Do not** use the Schneider Electric logo, wordmark or "Life Is On" tagline, and nothing that suggests Schneider endorsement. Only mention Schneider as the hackathon host.
- **Fonts:** a bold sans for titles (e.g. Montserrat or Poppins) and a regular sans for body (e.g. Inter or Open Sans).
- **Icon set:** line icons for battery, sun, house, shield, lightning bolt, phone, wrench/lineman, hospital cross.
- **Logo idea:** a shield (Kavach) with a lightning bolt inside, wordmark "GridKavach".
- **Rules:**
  - Max ~40 words of body text per slide.
  - One visual per slide.
  - Every number carries a small source line at the bottom (font size 8–9).
  - Labels such as "Target" and "Assumption" must stay visible on the slide.

---

## Slide 1: Title

**Title:** GridKavach
**Subtitle:** Dependable, safe power for India's solar-era neighbourhoods
**Tagline:** Forecast the gap · Share the battery · Protect the essentials · Shield the line
**Footer:** Challenge 03: Grid Reliability (Renewable Intermittency) · Team [TEAM NAME] · [COLLEGE]

**Visual:** full dark-green (`#009530`) background with white text. City rooftops with solar panels at dusk; a glowing shield outline over a power line.

**Speaker notes:** GridKavach is a neighbourhood flexibility and protection system for high-renewable distribution feeders. It keeps power dependable when solar falls short, and keeps people safe on a grid full of rooftop solar, batteries and inverters.

---

## Slide 2: The problem moved to the night

**Title:** India no longer runs short at 3 pm. It runs short at 10:45 pm.

**Body:**
- On the record 270.8 GW peak day (21 May 2026), the shortage during solar hours was **0.18 GW**, and at night it was **2.57 GW**.
- Solar reached **168 GW**, including **32.6 GW rooftop** (Aug 2026), with a record **44.6 GW** added in FY2026.
- **50 lakh+** homes now have rooftop solar under PM Surya Ghar.
- Clean power is abundant at noon and scarce after sunset.

**Visual:** a 24-hour "duck curve" line chart with solar output as a yellow area and demand as a charcoal line. Two shortage bars: a tiny one at 3 pm (0.18 GW) and a big red one at 10:45 pm (2.57 GW).

**Sources (footer):** Down To Earth (May 2026) · MNRE physical progress (31 Aug 2026) · JMK Research FY2026 · Swarajya / PM Surya Ghar (Aug 2026)

**Speaker notes:** India's shortages have moved from the daytime to the evening. As solar scales, the gap after sunset grows, and DISCOMs' main tool for it is still rotational load shedding.

---

## Slide 3: Who pays the price

**Title:** On a low-income feeder, the gap means darkness, and more power sources mean more danger.

**Three panels:**
1. **Darkness:** two in five urban households face a daily outage (IRES 2020), and about 34% kept kerosene as backup (Prayas 2019). Rotational load shedding cuts whole neighbourhoods: no study light, no fan, no clinic fridge.
2. **Unequal backup:** better-off homes buy private inverters, and poorer homes can't. Thousands of small batteries end up uncoordinated.
3. **Danger to crews:** 12,492 electrocution deaths in India in 2022 (NCRB). Linemen have been killed by **power coming in from a second source**, **home-inverter back-feed** (Goa 2024) and **lines switched back on during a shutdown** (Himachal; Lucknow, Sept 2026).

**Bottom strip:** only **17 of 72 DISCOMs** report SAIFI/SAIDI reliability indices, so the problem stays invisible in the data.

**Visual:** three side-by-side photo or illustration panels: a dark colony at night, a single house lit by an inverter, a lineman on a pole.

**Sources:** CEEW IRES 2020 · Prayas 2019 · NCRB ADSI 2022 (via WION) · The Goan · Tribune · Amar Ujala · Leap Blog (Sept 2025)

**Speaker notes:** Our hero setting is a dense, low-income urban neighbourhood of about 300–500 homes (assumption), with a clinic and a school on one feeder. The same distributed sources that could help (inverters, DG sets, batteries) also create back-feed risk for crews.

---

## Slide 4: The solution

**Title:** GridKavach: three layers, one feeder server

**Layer cards:**
1. **Gap Radar (forecast):** forecasts solar, load and battery 24 hours ahead, calculates the hourly intermittency gap, and sends feeder-stress and demand-response capacity signals to the DISCOM.
2. **Flex (bridge the gap):**
   - **Shift:** WhatsApp/SMS nudges move pumps, washing and e-rickshaw charging into solar hours.
   - **Share:** a community battery (second-life allowed) charges at noon and discharges into the gap under fair-access rules.
   - **Protect essentials:** if a gap remains, homes drop to an essential tier instead of going dark.
3. **Kavach (protect):**
   - **SafeLine:** a permit-to-work that blocks back-feed.
   - **LastGasp:** fault location from smart-meter power-loss alerts.
   - **ColdStart:** staged restoration so the feeder doesn't trip again.

**Tier strip:**
- Tier 0: clinic and school (always on)
- Tier 1: lights, fan, phone, medical devices
- Tier 2: fridge and TV
- Tier 3: AC, geyser, pump

**Visual:** three stacked horizontal layers (Forecast → Flex → Kavach) with icons. Next to them, a column of green checkmarks for the Challenge 03 goals: bridge the gap ✓, local ✓, affordable ✓, supports the DISCOM ✓.

**Footer fact:** built for India's smart-meter rollout: **20.33 crore meters sanctioned under RDSS, 7.24 crore installed** (30 Jun 2026).

**Speaker notes:** All four Challenge 03 goals map to a layer. We use the challenge's own language: feeder-level flexibility, community storage, demand response, forecasting and load shifting.

---

## Slide 5: Architecture

**Title:** Architecture: energy, data and money flows

**Diagram (rebuild in Canva):**
- **Top:** DISCOM control room (feeder-stress forecast, demand-response capacity, fault map, permit approvals)
- **Middle:** GridKavach feeder server: Gap Radar | Flex engine | Kavach (LastGasp, SafeLine, ColdStart) | feeder topology model
- **Bottom:**
  - community battery + rooftop PV (existing EMS)
  - smart meters in each home
  - households, shops, clinic
  - inverter registry
- **Protocols on arrows:** Modbus TCP · IEC 61850 · smart-meter head-end (IS 16444 / IS 15959 events) · WhatsApp/SMS

**Arrow colours:**
- 🟩 **Energy:** grid + PV → community battery → feeder → homes (tiered during gaps)
- 🟦 **Data:** meters and inverters → GridKavach → DISCOM; DISCOM → demand-response requests and permit approvals
- 🟧 **Money:**
  - households → local operator (monthly essential-power fee)
  - DISCOM → operator (demand-response payments)
  - DISCOM → GridKavach (per-feeder licence)
  - installers → GridKavach (registry fee)

**Callout:** follows CEA distributed-generation rules: an inverter must never energise a de-energised line, and must stop within 2 s of an unintended island. SafeLine verifies this in real time.

**Sources:** CEA Connectivity of DG Resources Regulations 2013 (amended 2019) · BRPL smart-meter tender spec (last-gasp requirement)

**Speaker notes:** This is the required architecture deliverable. A single edge server per feeder runs everything, so it doesn't need grid reinforcement.

---

## Slide 6: User journey

**Title:** 7:15 pm on a GridKavach feeder

**Timeline (across the top):**
- **3:00 pm:** Gap Radar predicts a 40-minute evening gap. The battery pre-charges and nudges go out.
- **7:15 pm:** the gap hits. The battery covers most of it, and homes drop to Tier 1. The clinic stays at full power.
- **7:42 pm:** a cable fault. LastGasp locates the section and restores the healthy sections.
- **7:50 pm:** a permit is requested. SafeLine finds an exporting home inverter and the battery, blocks both, verifies 0 V, and gets JE and lineman confirmation. The section is locked.
- **8:30 pm:** ColdStart restores power in 3 waves, with no re-trip.

**Four phone/desktop wireframes (below the timeline):**
1. **Household (phone):** "⚡ Evening shortage 7–8 pm. Your home is on Essential mode: lights, fan, charging ON." Plus a nudge: "Run the washing machine before 6 pm."
2. **Local operator (tablet):** battery state of charge, gap forecast, tier status by street.
3. **Lineman/JE permit screen (phone):** section S3 · back-feed sources: 2 found → 2 blocked ✓ · voltage 0 V ✓ · [Approve] [Confirm].
4. **DISCOM panel (desktop):** feeder-stress map, demand-response capacity in kW, fault location, open permits.

**Footnote:** design lesson from Eskom's load-limiting pilot: an SMS warning about 30 minutes ahead was critical to customer response.

**Speaker notes:** This is the demo we will build in the prototype phase. The four roles match the existing role-based access in our codebase.

---

## Slide 7: What exists vs what we add

**Title:** Proven building blocks, new combination

**Comparison matrix** (rows = capability, columns = existing solutions + GridKavach):

| Capability | Eskom load limiting (S. Africa) | TPDDL community battery (Delhi) | Utility outage systems (last-gasp) | UK Smart ReStart | ADMS/DERMS (Siemens, Schneider) | **GridKavach** |
|---|---|---|---|---|---|---|
| Essential power instead of blackout | ✓ (flat 10 A) | – | – | – | – | **✓ tiered + clinic priority** |
| Shared battery for the community | – | ✓ (DISCOM-owned) | – | – | partial | **✓ community-run, fair-access rules** |
| Fault location from meter alerts | – | – | ✓ | – | ✓ | ✓ (adapted) |
| Staged restoration | – | – | – | ✓ | partial | ✓ (adapted) |
| **Permit only after back-feed is verified blocked** | – | – | – | – | not found | **✓ new** |
| Built for low-income Indian feeders | ✗ (poorer Soweto got harsher cuts) | – | – | – | ✗ (enterprise) | **✓** |

**Takeaway line:** *We combine proven tools for a segment nobody serves, and add the safety interlock and fair rules that make them safe to hand to a community.*

**Sources:** SAGEN Eskom case study (2025) · Daily Maverick (Nov 2025) · Mercom (TPDDL community battery) · Renewable Energy World (AMI outage management) · LCP Smart ReStart · Siemens / Schneider ADMS pages

**Speaker notes:** We are honest about prior art. Each of the novelty claims (the SafeLine interlock, community-governed fair access, and the low-income focus) is "not found in surveyed products".

---

## Slide 8: Impact against a baseline

**Title:** Measured against today's load shedding

**Baseline (left box, red):** rotating load shedding (whole sections off) · faults found by switching ring main units one by one · everything re-energised at once · no back-feed check.

**Method (small text):** the same 30 days of seeded data plus evening-gap and fault scenarios, run under the baseline and under GridKavach in our simulator.

**Metrics table** (label the column clearly as **TARGET, to be validated in simulation**):

| Metric | Baseline | GridKavach target |
|---|---|---|
| **Essential-supply availability during intermittency windows** (headline) | 0% for the shed section | ≥ 95% of homes keep Tier-1 power |
| Household hours with zero supply / month | as shed | ↓ sharply (measured) |
| Local solar used locally | curtailed at noon | ↑ via battery + shifting |
| Evening peak drawn from the DISCOM | full | ↓ by battery + demand response |
| Fault location time | sequential switching | minutes |
| Back-feed exposures on a permitted section | unchecked | **0** |
| Re-trips on restoration | common after long outages | **0** |

**External anchors (bottom strip):**
- Eskom load limiting cut about **1 kW per meter**, with 70%+ response once communications were fixed.
- IEEE: cold-load surge up to **210%** of normal load, and motor inrush 5–8×.

**Sources:** SAGEN Eskom case study · IEEE PES PSRC WG D1 report

**Speaker notes:** Impact & Measurability is worth 25%, so we show the exact method and baseline. All GridKavach numbers are targets that our simulator will measure during the prototype phase. We do not claim results we haven't produced. Outage logs are SAIFI/SAIDI-ready, which supports the Electricity (Rights of Consumers) Rules 2020.

> ✏️ If you run the simulator before submitting, replace the targets with measured numbers and change the label to "Simulated result".

---

## Slide 9: Ownership and unit economics

**Title:** Essential power for every home, run by the community

**Ownership model (left):**
- **Owner/operator:** a residents' welfare association or women's self-help group cooperative owns the community battery and employs one trained local operator.
- **Fallback:** a DISCOM-owned battery with a self-help-group operator under a franchisee arrangement.
- **Maintenance:** installer annual maintenance contract for the battery and inverter; GridKavach software updated remotely.
- **DISCOM:** grid connection, demand-response programme, permit approvals, per-feeder licence.

**Unit economics (right). Show the formula and keep it labelled:**
- Battery size = 400 homes × 150 W essential × 3 gap hours ÷ 0.8 depth of discharge ≈ **225 kWh** *(assumption)*
- Cost floor from a real tender: Rajasthan 1 GW / 2 GWh battery cleared at **₹1.775 lakh/MW/month** → about ₹2.4 lakh/year for 225 kWh → **about ₹50 per household per month** *(team calculation; a utility-scale floor, so neighbourhood scale will cost more)*
- **Revenue streams:** household fee + DISCOM demand-response payments + evening energy arbitrage + per-feeder licence + installer registry fee

**Indian precedents (bottom):**
- TPDDL's 0.52 MWh community battery already backs up "preferential consumers".
- BRPL's Kilokari 20 MW / 40 MWh battery serves about 1 lakh residents.
- Battery packs are now about **$70/kWh** for stationary storage (BNEF 2025).

**Visual:** money-flow waterfall, with a big callout: **"≈ ₹50 / home / month (floor)"**.

**Sources:** Saur Energy (Rajasthan tender, Oct 2025) · BNEF via ESS News (Dec 2025) · IEEFA (2026) · Mercom / Energetica (TPDDL) · pv magazine India (BRPL Kilokari)

**Speaker notes:** The affordability test is essential power for every home for less than what one family spends on a private inverter. The final comparison will use a sourced inverter price.

---

## Slide 10: Sustainability

**Title:** Sustainable twice: cleaner energy, lasting ownership

**Planet (left):**
- Uses midday rooftop solar locally instead of curtailing it (32.6 GW rooftop PV already installed).
- Displaces diesel DG sets and kerosene during evening gaps (measured by our carbon-analytics module).
- Second-life EV batteries are allowed in the design.
- Adds the kind of distributed storage India needs: an estimated **411 GWh** of battery storage by 2031–32 (CEA).

**People and institutions (right):**
- Local jobs: a trained self-help-group operator for each feeder.
- Community governance: fair-access rules and an audit log for every rationing decision.
- Long-term operation and maintenance through the DISCOM licence and installer contract.
- Safer work for line crews.

**Visual:** two columns ("Planet" 🌍 / "People" 🤝) with 3–4 icon bullets each.

**Sources:** MNRE · Down To Earth (CEA storage estimate) · GridKavach simulator (diesel avoided)

**Speaker notes:** Sustainability carries 15% of the score. GridKavach is environmentally sustainable because it maximises local renewable use and displaces diesel, and institutionally sustainable because the community owns and runs it.

---

## Slide 11: Roadmap

**Title:** Six weeks to a working feeder simulation, then a pilot

**Prototype phase (Gantt, 11 Oct – 22 Nov 2026):**

| Week | Dates | Build |
|---|---|---|
| 1 | 11–17 Oct | Feeder topology model + smart-meter simulator |
| 2 | 18–24 Oct | Gap calculation + tier rationing in the EMS |
| 3 | 25–31 Oct | LastGasp fault location + comms-loss fallback |
| 4 | 1–7 Nov | SafeLine permit workflow + section lock |
| 5 | 8–14 Nov | ColdStart wave planner + 4 role screens |
| 6 | 15–22 Nov | 30-day baseline-vs-GridKavach runs, scoreboard, demo video |

**After the prototype (arrow):**
1. **Pilot:** one low-income urban feeder with a DISCOM and an RWA/SHG.
2. **Expand:** peri-urban feeders (SafeLine for pole work) and rural feeders (LastGasp for long lines, pump shifting).
3. **Scale:** a low-voltage community module for ADMS / EcoStruxure Grid.

**Risks and mitigations (small box):**
- Communication failures → edge server runs autonomously, with SMS fallback.
- Power-loss alerts lost in big outages → head-end filtering plus inference from loss of communication.
- Inverters that can't be controlled remotely → detect the source and block the permit.
- Fairness concerns → equal essential allowance, transparent rules, audit log.

**Speaker notes:** The prototype plan is concrete and already half-built (see the next slide).

---

## Slide 12: Team and head start

**Title:** Team GridKavach, with a working SCADA already built

**Team (left, 1–4 members):**
- [Name 1]: [Role, e.g. Power systems & EMS] · [Year, Branch, College]
- [Name 2]: [Role, e.g. ML & forecasting]
- [Name 3]: [Role, e.g. Full-stack & UI]
- [Name 4]: [Role, e.g. Economics & field research]

**Head start (right):** our existing open-source microgrid SCADA/EMS, about 11k lines ([GitHub link]):

| Already built | Becomes in GridKavach |
|---|---|
| EMS with 4 dispatch modes + Q-learning battery scheduler | Community battery dispatch with fair access |
| Load, solar and wind forecasters | Gap Radar |
| Island detection + anomaly detector | Back-feed detection for SafeLine |
| Modbus TCP / IEC 61850 / OPC UA simulators | Inverter interlock + breaker switching |
| Alarms + 5-role access control + double confirmation | Permit-to-work workflow |
| Failure simulation + carbon analytics | Demo scenarios + diesel-avoided metric |

**Closing line:** *GridKavach: no home fully dark, no crew unprotected.*

**Visual:** team photos in circles on the left; reuse table on the right; a screenshot of the existing dashboard (single-line diagram) in the corner.

**Speaker notes:** About 75% of the platform exists today, so the six-week prototype plan is realistic.

---

## Before you submit (not a slide)

- [ ] Fill in the team name, members and college on slides 1 and 12.
- [ ] Push the code to `scadaheck`, or put the `scada` repo link on slide 12.
- [ ] Slide 8: keep the "TARGET" labels unless you have run the simulator.
- [ ] Slide 9: add a sourced private-inverter price for the affordability comparison, or remove that line.
- [ ] Use your own diagrams and screenshots (the rules ban "unauthorized AI-generated content").
- [ ] Make the 300–500 word description match these slides and figures exactly.
- [ ] Full sources: `reports/GridKavach pitch deck research.md`
