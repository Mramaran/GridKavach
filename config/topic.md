# Ideation Topic Configuration

## Topic
Non-obvious, SCADA-centric innovation for the **Schneider Electric Yuva Yodha Energy Tech Hackathon 2026** (India, full-time student teams of up to 4, submission deadline **2026-10-04**).

## Purpose
Find the single most differentiated, winnable idea that builds on the team's existing SCADA/EMS codebase, then shortlist runners-up.

## Base asset (must be reused)
`github.com/veneshvpm/scadaheck` (Nexus SCADA), a microgrid SCADA/EMS:
- React/TS + MUI front end, FastAPI + WebSocket back end, SQLAlchemy (SQLite/Postgres), Docker, MQTT
- Animated single-line diagram (SLD) with energy flows
- ML forecasting (solar, wind, load, battery health) using RandomForest/LinearRegression
- Alarm management with timeline and double confirmation for critical controls
- 5-role RBAC (viewer to admin), JWT
- Modbus TCP simulator; 30-day seeded telemetry
- Secondary repo `veneshvpm/scada`: CSV datasets (grid exports), docs, report scripts

## Challenges (pick one)
01 Sustainable Agriculture · 02 Smart Buildings · 03 Grid Reliability · 04 Smart Manufacturing

## Constraints
- Must be SCADA-native: control, protection, telemetry, field protocols, operator workflow. Not a generic analytics app.
- **Avoid generic AI ideas:** "dashboard + ML forecasting", P2P energy trading, chatbots, generic carbon calculators, generic digital twins
- Must fit Indian conditions (DISCOMs, load shedding, smart-meter rollout, SMEs, farmers, low-income users)
- Software or simulation only; no physical hardware needed
- Buildable or demoable from scadaheck in about 3 days
- Needs quantifiable impact against a baseline and a credible business or ownership model
- Should appeal to Schneider Electric (EcoStruxure, grid automation, SCADA heritage)

## Prior candidate (benchmark to beat)
**LifeLine Grid** (Ch 03): forecast, shift, then ration tiered loads instead of rotational load shedding; urban/village/island modes.

## Output format per idea
Name · challenge · one-line hook · problem · mechanism (what the SCADA actually does) · why it is not a generic AI idea · scadaheck reuse % · new work needed · impact metric and baseline · business model · Schneider appeal · risks

## Depth
standard

## Quantity per run
10

## Diversity mode
balanced (spread across the 4 challenges, weighted toward SCADA-native control mechanisms)
