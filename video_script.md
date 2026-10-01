# GridKavach: Pitch Video Script

**Length:** about 2 min 45 s (≈ 400 words of narration at ~145 words/min)
**Style:** technical demo. Screen recording of our SCADA plus deck visuals, one narrator, light background music.
**Goal:** score on all five criteria in under 3 minutes: Problem 20% · Architecture 20% · **Impact 25%** · Feasibility 20% · Sustainability 15%.

> **Honesty rule:** say "already built" only for features in our `scada` code (single-line diagram, forecasts, EMS / Q-learning, island mode, Modbus · IEC 61850 · OPC UA simulators, alarms, role-based access). The current UI has no double-confirmation dialog, so don't claim one in the demo. Say **"prototype screens"** or **"we will build"** for SafeLine / LastGasp / ColdStart, and **"target"** for every impact number.

---

## Shot list and narration

### 0:00 – 0:12 · Hook *(Problem 20%)*
**Visual:** black screen → a city skyline at dusk; lights in one neighbourhood switch off block by block. On-screen text: **"10:45 pm"**.
**On-screen text:** *India no longer runs short at 3 pm. It runs short at 10:45 pm.*

> **Narration:** "On India's record peak day this year, the power shortage during solar hours was point-one-eight gigawatts. At night, it was two-point-five-seven. Our grid is going solar, and the dark hours are moving to the evening."

---

### 0:12 – 0:35 · Problem *(Problem 20%)*
**Visual:** deck slide 2 (bar chart animating 0.18 → 2.57 GW), then slide 3 (three cards appearing one by one).
**On-screen text:** "2 in 5 urban homes: daily outage" · "12,492 electrocution deaths (2022)" · "Only 17 of 72 DISCOMs report SAIDI"

> "When supply falls short, a DISCOM's only tool is rotational load shedding: a whole low-income neighbourhood goes dark. No study light, no fan, no clinic fridge. Richer homes buy inverters, so the feeder fills with uncoordinated batteries, and that creates a second danger. Linemen have been killed by back-feed from a home inverter, or by a line switched back on during a shutdown."

---

### 0:35 – 0:55 · Solution *(Idea quality)*
**Visual:** slide 4. The three layers light up in turn: Gap Radar → Flex → Kavach. The tier chips T0–T3 slide in.
**On-screen text:** **GridKavach: Forecast the gap · Share the battery · Protect the essentials · Shield the line**

> "GridKavach is a SCADA layer for one feeder. **Gap Radar** forecasts the evening shortfall 24 hours ahead. **Flex** shifts loads into solar hours and dispatches a shared community battery. If a gap remains, every home drops to an essential tier (lights, fan, phone, medical) instead of going dark, and the clinic stays at full power. And **Kavach** keeps the crews safe."

---

### 0:55 – 1:40 · Technical demo *(Architecture 20%, Feasibility)*
**Visual: screen recording of our running SCADA** (`scada` repo, local run).

| Time | Show on screen | Narration |
|---|---|---|
| 0:55 | Dashboard → animated single-line diagram with solar, wind, battery, grid, load | "This is our SCADA, already running: about eleven thousand lines, React and FastAPI, live over WebSockets." |
| 1:05 | Forecast page (solar / load charts) | "Gap Radar starts from our existing ML forecasters for solar, wind, load and battery state." |
| 1:12 | EMS / controls page: dispatch mode, battery charge/discharge | "Our EMS and Q-learning scheduler already dispatch the battery against tariffs. We add a fair-access rule and a restoration reserve." |
| 1:20 | Protocols page: Modbus registers, IEC 61850 breaker node | "It speaks Modbus TCP, IEC 61850 and OPC UA. That's how we read inverters and breakers, and how SafeLine writes the export-block command." |
| 1:28 | Log in as **engineer**, toggle the **grid off** → EMS switches to island mode (`ISLAND_BALANCED`), alarm appears. Optionally show the "UNAUTHORIZED" message when a viewer tries the same toggle | "When the grid fails, our EMS detects it and keeps running in island mode, and only authorised roles can switch the grid. That island state is exactly what SafeLine watches for: if a source is still feeding a section that should be dead, the permit is blocked." |

> **Recording tip:** keep the cursor slow, zoom in on each panel (Win + Plus), and blur the login screen.

---

### 1:40 – 2:00 · The 7:50 pm moment *(Innovation)*
**Visual:** slide 6, zooming into the timeline and then the **lineman permit screen** mockup ("Back-feed: 2 found → 2 blocked ✓ · 0 V ✓ · Approve"). Then slide 7 (comparison table), with **"✓ new"** pulsing.
**On-screen text:** **"No permit until back-feed is verified blocked."**

> "Here's the part nobody else does. At 7:50 a cable fault: LastGasp locates it from smart-meter power-loss alerts. Before a lineman touches it, SafeLine finds every back-feed source on that section, blocks their export, verifies zero volts, and only then releases the permit. Then ColdStart brings power back in waves, so the feeder doesn't trip again. Load limiting, community batteries and outage maps exist. A permit interlocked with distributed sources, run for a low-income community, is what we found missing."

---

### 2:00 – 2:20 · Impact *(Impact & Measurability 25%)*
**Visual:** slide 8. The baseline column appears in red, then the target column in green. Highlight the headline row.
**On-screen text:** **Essential supply in gap hours: 0% → ≥95% of homes (TARGET)** · Back-feed exposures → 0 · Re-trips → 0
**Small caption:** *Targets, to be validated in simulation*

> "We measure ourselves against today's load shedding. We run the same thirty days of data both ways in our simulator. Our headline target: at least ninety-five percent of homes keep essential power during gap hours, against zero today. Zero back-feed exposures on permits, and zero re-trips. Eskom's load limiting saved about a kilowatt per meter, so these targets have a real precedent."

---

### 2:20 – 2:35 · Ownership and sustainability *(Feasibility & Affordability 20%, Sustainability 15%)*
**Visual:** slide 9, the big **≈ ₹50 / home / month** callout. Quick cut to slide 10's stat tiles.
**On-screen text:** "Run by a women's SHG cooperative" · "≈ ₹50/home/month (cost floor)"

> "A women's self-help group owns the battery and runs it locally. Our cost floor, from a real state battery tender, is about fifty rupees per home per month. It uses rooftop solar locally, displaces diesel, and creates a local job on every feeder."

---

### 2:35 – 2:50 · Roadmap and close
**Visual:** slide 11 Gantt animating week by week → slide 12 closing band.
**On-screen text:** **GridKavach: No home fully dark. No crew unprotected.** · Team [TEAM NAME] · [COLLEGE]

> "Seventy-five percent of the platform already exists. Give us the six-week prototype window and we'll deliver a working feeder simulation with real numbers. GridKavach: no home fully dark, no crew unprotected."

---

## Production checklist

- [ ] **Record the SCADA demo first** (0:55–1:40). Run the `scada` repo locally and practise the click path 2–3 times. Use OBS or the Xbox Game Bar (Win + G) at 1080p.
- [ ] **Deck visuals:** in PowerPoint, File → Export → Create a Video (1080p), or screen-record slideshow mode, and cut the slide segments listed above.
- [ ] **Voice-over:** record separately in a quiet room with a phone or headset mic. Speak slightly slower than normal. Target total length ≤ 2:55.
- [ ] **Captions:** burn in subtitles. Many judges watch muted.
- [ ] **Music:** royalty-free, low volume (−20 dB under the voice), e.g. YouTube Audio Library.
- [ ] **Keep these labels visible on screen:** "TARGET", "prototype screens", "cost floor (team calculation)".
- [ ] **No Schneider logo** anywhere; the hackathon name in text is fine.
- [ ] **Team:** a 2-second face cam or team photo at the end adds trust (optional).
- [ ] **Editing:** Clipchamp (built into Windows) or DaVinci Resolve (free).

## Timing summary

| Segment | Time | Criterion |
|---|---|---|
| Hook | 0:00–0:12 | Problem |
| Problem | 0:12–0:35 | Problem |
| Solution | 0:35–0:55 | Idea quality |
| Live SCADA demo | 0:55–1:40 | Architecture, Feasibility |
| SafeLine moment + prior art | 1:40–2:00 | Innovation |
| Impact vs baseline | 2:00–2:20 | **Impact 25%** |
| Ownership + sustainability | 2:20–2:35 | Affordability, Sustainability |
| Roadmap + close | 2:35–2:50 | Feasibility |
