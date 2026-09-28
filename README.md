# GridKavach

Dependable, safe power for India's solar-era neighbourhoods.

GridKavach is our entry for the **Schneider Electric Yuva Yodha Energy Tech Hackathon 2026, Challenge 03: Grid Reliability (Renewable Intermittency)**. It extends a working microgrid SCADA/EMS into a feeder-level system that keeps homes on essential power when solar falls short, and keeps line crews safe on a grid full of rooftop solar, batteries and inverters.

Demo video: [VIDEO LINK]

## The idea

| Layer | What it does |
|---|---|
| Gap Radar | Forecasts the evening shortfall a day ahead and shows the DISCOM how much load the feeder can shift |
| Flex | Shifts flexible loads into solar hours, dispatches a shared community battery under fair-access rules, and drops homes to an essential tier instead of a blackout |
| Kavach | Safety layer: SafeLine (permit-to-work released only after back-feed is blocked and 0 V verified), LastGasp (fault location from smart-meter power-loss alerts), ColdStart (staged restoration with no re-trip) |

The SCADA core in `scada/` runs today. Gap Radar, Flex and Kavach are the modules we build on top of it during the prototype phase. Full design: [docs/superpowers/specs/2026-10-01-gridkavach-design.md](docs/superpowers/specs/2026-10-01-gridkavach-design.md).

## Repository structure

```
scada/            Microgrid SCADA/EMS (React + FastAPI), imported from github.com/veneshvpm/scada
  backend/        FastAPI server, EMS + Q-learning dispatch, ML forecasters,
                  Modbus TCP / IEC 61850 / OPC UA / CAN simulators
  frontend/       React HMI: single-line diagram, forecasts, EMS control, alarms
  docs/           Architecture and deployment notes
docs/             GridKavach concept design
reports/          Research report behind the pitch
research_notes/   Source notes (judging criteria, India grid facts, prior art)
project_description.md   Submission write-up
slide_content.md         Pitch deck content
video_script.md          Demo video script
```

## Running the SCADA

Requires Python 3.10+ and Node.js 20+.

```bash
cd scada/backend
pip install -r requirements.txt
python main.py            # API + WebSocket on http://localhost:8000
```

```bash
cd scada/frontend
npm install
npm run dev               # HMI on http://localhost:5173
```

Control roles (password = username): `admin`, `engineer`, `operator`, `viewer`. Try the "Energy Green" theme, then isolate the Utility Grid as `engineer` to see island mode.

## Team

Team Ember Syndicate, Coimbatore Institute of Technology.
