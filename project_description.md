**GridKavach: a SCADA that keeps the lights on and the linemen safe**

At 3 pm, India has more solar power than it can use. At 10:45 pm, it runs short. On this year's record peak day, the shortfall during solar hours was 0.18 GW; at night it was 2.57 GW. When that gap reaches a low-income feeder, the DISCOM's main tool is rotational load shedding, and the whole neighbourhood goes dark, including the study lamps, the fans in a heatwave and the clinic fridge. Families who can afford it buy inverters, which nobody coordinates. They are also a hazard: line crews in India have been killed by back-feed from a home inverter, and by lines switched back on during a shutdown.

GridKavach builds on a microgrid SCADA/EMS we have already written, about 11,000 lines of React and FastAPI with live WebSocket telemetry. It has an animated single-line diagram, ML forecasts for solar, wind, load and battery, a Q-learning battery scheduler, island-mode detection, role-based access, and Modbus TCP, IEC 61850 and OPC UA interfaces. We are extending it from one microgrid to a whole neighbourhood feeder, in three layers.

Gap Radar forecasts the evening shortfall a day ahead and shows the DISCOM how much load the feeder can shift. Flex closes the gap. It nudges households to run pumps and washing machines in solar hours and dispatches a shared community battery under fair-access rules. If supply is still short, each home drops to an essential tier (lights, fan, phone, medical devices) and keeps power, while the clinic and school stay fully on. Kavach handles safety. LastGasp locates cable faults from smart-meter power-loss alerts. SafeLine is a digital permit-to-work: before a crew touches a section, the SCADA finds every back-feed source, blocks its export, confirms zero volts, and only then releases the permit. ColdStart brings the section back in waves so the feeder doesn't trip again.

Some of these ideas exist elsewhere, in Eskom's load limiting, Tata Power-DDL's community battery and smart-meter outage maps. We found no product that interlocks permits with distributed sources, and none that pairs this with community-run sharing rules for low-income urban feeders.

We will compare GridKavach with today's load shedding by running the same 30 days of data both ways in our simulator. Our targets are at least 95% of homes keeping essential power during gap hours (0% today), zero back-feed exposures on permits, and zero re-trips. A women's self-help group would own and run the battery; our cost floor, based on a real state battery tender, is about ₹50 per home per month.

The SCADA core runs today, and Gap Radar, Flex and Kavach are what we will build in the six-week prototype window. Low-income households, small shops and clinics, line crews and DISCOMs all gain a feeder they can see and rely on.

▶ **Watch our demo (2:41):** [VIDEO LINK]
