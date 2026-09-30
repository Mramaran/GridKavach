# Prior Art & Competitive Landscape — GridKavach Novelty Positioning

Scope: 2020-2026 sources. About 22 search/fetch calls. Some sub-questions were only partly covered; see the Gaps sections. "Not found" means I did not find it in this search. It does not prove the thing doesn't exist.

## Q1. Existing products (utility ADMS/DERMS vendors, AMI/OMS, mini-grid and Indian players): which features overlap?

### Takeaway
Big-vendor ADMS/DERMS platforms already cover switching management, FLISR, staged restoration and DER flexibility. AMI last-gasp outage localisation to the service-transformer level is a standard, mature feature. Mini-grid metering platforms such as SparkMeter already do per-customer load limiting. GridKavach can't claim novelty on any of these parts alone. What it can claim is the combination, the ownership model, and the low-income Indian grid-connected feeder context.

### Cited Findings
- **Schneider EcoStruxure ADMS** describes itself as covering monitoring, analysis, control, optimisation, planning and training on one network model, with outage response and DER management. — [Schneider EcoStruxure ADMS](https://www.se.com/au/en/product-range/61751-ecostruxure-adms/)
- Schneider's GridOps Management Suite 3.10 documentation includes separate "Switching Management" and "Switching Validations" functional specifications. This means formal switching-plan and validation tooling exists in the incumbent ADMS. — [Schneider ADMS 3.10 documentation update](https://smartgrid.schneider-electric.com/s/blog-article/a05QO00000EiCVFYA3/adms-310-hf9-product-documentation-update)
- Schneider says its ADMS comes "with embedded DERMS" (Forrester TEI study, July 2026). — [Schneider blog, 2026](https://blog.se.com/energy-management-energy-efficiency/2026/07/03/unlocking-grid-efficiency-and-roi-findings-from-a-forrester-total-economic-impact-study-of-schneider-electrics-ecostruxure-adms-with-embedded-derms/)
- **Siemens Gridscale X LV Management** is marketed as a "co-pilot" for low-voltage grid instability, with a claimed 30% reduction in outages. — [Siemens press release](https://press.siemens.com/global/en/pressrelease/siemens-reveals-co-pilot-flexible-low-voltage-grid-management-new-gridscale-x-software)
- **Siemens Gridscale X Flexibility Manager** monitors grid conditions, predicts overloads, and identifies flexibility from EVs, heat pumps, batteries and distributed generation. It claims up to 20% more capacity utilisation and up to 40% savings on grid investment. This overlaps conceptually with GridKavach's "Gap Radar" (forecast plus flexibility). — [Siemens Flexibility Manager press release](https://press.siemens.com/global/en/pressrelease/siemens-unveils-flexibility-software-increase-electricity-grid-capacity-moving-towards); [product page](https://www.siemens.com/en-us/products/gridscale-x/flexibility-manager/)
- Siemens Gridscale X DER Insights covers hosting-capacity assessment and identifying DER flexibility. — [Siemens DER Insights](https://www.siemens.com/en-us/products/gridscale-x/der-insights/)
- Siemens sells a separate Outage Event Management product. — [Siemens OEM datasheet](https://assets.new.siemens.com/siemens/assets/api/uuid:8708a30d-c812-4b5f-bac2-bc5214be7f1e/outage-event-management-3-0-datasheet.pdf)
- **Last-gasp (AMI/OMS) is mature prior art.** Last-gasp messages from AMI endpoints let an OMS locate outages to the service-transformer level, which cuts truck rolls and restoration time. — [Renewable Energy World: Enhancing Outage Management with AMI](https://www.renewableenergyworld.com/power-grid/outage-management/enhancing-outage-management-with-ami/)
- Known limitation: in large outages, message collisions and bandwidth limits can block up to about 80% of last-gasp messages. Filtering middleware between AMI and OMS is recommended. — [Renewable Energy World](https://www.renewableenergyworld.com/power-grid/outage-management/enhancing-outage-management-with-ami/)
- Indian IT services firms are already pitching ADMS and AMI integration for Indian DISCOMs. — [Cyient blog, 2024](https://www.cyient.com/blog/2024/7/enhancing-grid-efficiency-and-reliability-integrating-adms-and-ami); [NASSCOM community](https://community.nasscom.in/index.php/communities/energy-utilities/enhancing-grid-efficiency-and-reliability-integrating-adms-and-ami)
- Patents exist on locating faults on distribution networks and on MDM systems with outage management. — [US 8810251](https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/8810251); [US 8462014](https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/8462014); [US 9103854](https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/9103854)
- **SparkMeter** (used by Husk Power and others) offers real-time monitoring, pay-as-you-go, load control, and "limiting consumption to specific groups during times of high demand or low supply". It also offers per-customer load limits and demand response. This is a direct precedent for group-wise and tiered rationing, but in mini-grid settings. — [Engineering for Change: SparkMeter](https://www.engineeringforchange.org/solutions/product/sparkmeter/); [Global Innovation Fund: SparkMeter](https://www.globalinnovation.fund/investments/spark-meter)
- Husk Power worked with SparkMeter from 2015 on customer-level metering and control. — [Wikipedia: Husk Power Systems](https://en.wikipedia.org/wiki/Husk_Power_Systems)
- **Okra Solar** runs plug-and-play "mesh-grids" that connect household solar and batteries, with a "Pod" that uses ML and remote monitoring to distribute power across households. This is a precedent for shared or pooled storage dispatch, but it is off-grid. — [ARE case study: Okra mesh-grid Nigeria](https://renewelec.org/case-study/okra-business-model-revolution-with-mesh-grid-nigeria/); [ESI Africa](https://www.esi-africa.com/renewable-energy/okra-mesh-grid-an-african-power-energy-elites-smart-solutions-project/)
- **Smart Power India** (Rockefeller Foundation) has facilitated 500+ mini-grids with developers including TPRMG, Husk, OMC, Tara Urja and Mlinda. — [pv magazine India](https://www.pv-magazine-india.com/press-releases/smart-power-india-facilitates-the-worlds-largest-portfolio-of-500-mini-grids/); [T&D India](https://www.tndindia.com/smart-power-india-commissions-500th-mini-grid-portfolio-capacity-crosses-15-mw/amp/)
- **Mlinda** mini-grids in Gumla, Jharkhand serve domestic, productive and institutional loads, including hospitals and health centres. Health centres there typically draw 1-5 kW. — [ARE case study: Mlinda](https://www.ruralelec.org/case-study/mlinda-25-kwp-dre-based-mini-grids-india/); [Mlinda](https://mlinda.org/democratising-energy-supply/)
- Shell Foundation's 2024 report gives an overview of off-grid/distributed utility models in emerging markets. — [Shell Foundation DCU report](https://shellfoundation.org/wp-content/uploads/2024/08/Shell-Foundation-Bridging-the-Gap-DCU-report.pdf)

### Inferences
- Overlap map (GridKavach module, then the closest prior art):
  - Gap Radar: Siemens Flexibility Manager / DER Insights and Schneider ADMS+DERMS.
  - Flex rationing: SparkMeter group load-limits and Eskom load limiting (Q2).
  - Community battery: TPDDL CESS and Australian community batteries (Q3).
  - LastGasp: standard AMI-OMS integration.
  - ColdStart: academic staged restoration plus UK Smart ReStart (Q5).
  - SafeLine: ADMS switching management and validation (Q4).
- The incumbents sell to the utility control room at enterprise scale. The mini-grid players (SparkMeter, Okra, Husk, Mlinda) work off-grid or in rural mini-grids. Neither group targets a grid-connected urban low-income feeder run by a community operator.
- Defensible differentiator: GridKavach is a feeder-scale bundle with community governance. It is not a new algorithm category.

### Gaps
- I didn't research GE Vernova / Hitachi Energy ADMS, Itron, Landis+Gyr, Zenatix, Mysun, SunAlpha or Oorja product pages directly. Their overlap isn't verified here.
- I found no source showing any of these vendors offering tiered "essential-load" rationing on grid-connected urban feeders in India.

## Q2. Load limiting / "brownout instead of blackout" via smart meters: precedents, results, criticisms

### Takeaway
Eskom's smart-meter load limiting (10 A instead of a blackout during Stages 1-4) is the strongest and best-documented precedent for GridKavach's "every home keeps lights/fan/phone" idea. Its results are real: about 15.3 MW, about 1 kW per meter, and 70%+ response once comms were fixed. But it was piloted in affluent suburbs. Poorer, high-density areas like Soweto instead got "load reduction" (longer blackouts), which caused equity complaints. Academic "soft load shedding" and fair-allocation work also exist. GridKavach's added elements are appliance-tier logic, clinic priority, and a battery-backed floor.

### Cited Findings
- Eskom piloted load limiting from June to September 2023 in Fourways (Johannesburg), expanding to Riversideview. It went to national rollout in January 2024. — [SAGEN / City Energy case study (Eskom load limiting pilot, PDF)](https://www.cityenergy.org.za/wp-content/uploads/2025/03/Eskom-Load-limiting-pilot.pdf)
- Mechanism: the meter's limit is cut from the normal 60/80 A connection to 10 A during load-shedding Stages 1-4; the exemption ends at higher stages. The customer chooses which appliances to keep on. If the load isn't reduced, the meter temporarily disconnects and shows "Power Overload" on the Customer Interface Unit. — [SAGEN PDF](https://www.cityenergy.org.za/wp-content/uploads/2025/03/Eskom-Load-limiting-pilot.pdf)
- Results: about 9,000 meters at the start, 12,506 by September 2023. Average demand reduction was 15.3 MW across seven events in the last week of June 2023, and about 1 kW per meter could be relied on. Cost was about R2.4-3.5 million per MW, comparable to peak-clipping DSM at R3.5 million per MW. — [SAGEN PDF](https://www.cityenergy.org.za/wp-content/uploads/2025/03/Eskom-Load-limiting-pilot.pdf)
- Lessons: response was initially low because of faulty data concentrators, faulty meters, weak signal and bad SIMs. It improved to at least 70% once these were fixed. The case study calls CIUs in every home and SMS reminders 30 minutes ahead critical. — [SAGEN PDF](https://www.cityenergy.org.za/wp-content/uploads/2025/03/Eskom-Load-limiting-pilot.pdf)
- The Fourways site was deliberately chosen as "affluent", with high per-capita use and a peaky profile. Impact depends on socio-economic profile. — [SAGEN PDF](https://www.cityenergy.org.za/wp-content/uploads/2025/03/Eskom-Load-limiting-pilot.pdf)
- Eskom also piloted load limiting in Western and Eastern Cape (Sunningdale and Rivergate in Cape Town), with up to 10 A for essential appliances. — [Green Building Africa](https://www.greenbuildingafrica.co.za/eskom-will-be-piloting-load-limiting-in-cape-town-and-eastern-cape/)
- Eskom's smart meter brochure (January 2024) describes the customer-facing load-limiting proposition. — [Eskom smart meter brochure](https://www.eskom.co.za/distribution/wp-content/uploads/2024/01/20240129-SMART-METER-BROCHURE-rev2.pdf)
- **Criticism / equity:** Soweto residents complained of being hit by both load shedding and "load reduction". Load reduction targets high-density areas with illegal connections and strained infrastructure. — [Sunday Independent, 2022](https://sundayindependent.co.za/news/2022-06-21-soweto-residents-feel-the-brunt-of-eskoms-load-reduction/)
- Prepaid customers who pay still face load reduction (November 2025). — [Daily Maverick, 2025](https://www.dailymaverick.co.za/article/2025-11-10-soweto-residents-decry-ongoing-power-cuts-under-eskoms-load-reduction-programme/)
- Smart-meter resistance is strongest in Gauteng and KZN, according to the Eskom chair (September 2026). — [Sowetan, 2026](https://www.sowetan.co.za/news/2026-09-15-firmest-resistance-to-smart-meters-in-gauteng-and-kzn-eskom-chair-mteto-nyati/)
- Eskom proposed a R16 billion smart-meter rollout to every household (2023) and is reported to be more than 50% behind on rollout. — [IOL, 2023](https://iol.co.za/business-report/economy/2023-04-25-eskom-proposes-r16bn-smart-meter-rollout-to-all-households/); [ITWeb](https://www.itweb.co.za/article/eskom-more-than-50-behind-on-smart-meter-rollout/o1Jr5qxPY99qKdWL)
- A related Eastern Cape curtailment project faced initial community resistance before getting "back on track" (January 2024). — [The Herald via PressReader](https://www.pressreader.com/south-africa/the-herald-south-africa/20240116/281535115842994)
- **India:** demand limiting that enforces sanctioned load is listed as a built-in AMI capability in India's smart-metering ecosystem. — [NES India blog](https://nesindia.co/blog/smart-metering-india-rdss-ami-amisp-atc-losses)
- RDSS targets 25 crore smart meters by March 2028. About 6.00 crore were installed of 20.33 crore sanctioned as of August 2026. — [Kimbal RDSS update](https://kimbal.io/blog/rdss-scheme-state-wise-update/); [Earth Energy Log](https://earthenergylog.com/articles/india-smart-meters-2026)
- Prayas (Pune) analysis of Indian smart metering, "a work in progress". — [Prayas Energy Group](https://energy.prayaspune.org/power-perspectives/smart-metering-in-india-a-work-in-progress)
- **Electricity (Rights of Consumers) Rules 2020** were amended in 2021, 2022, 2023 and 2024. DISCOMs must compensate consumers if they miss reliability standards. The February 2024 amendment simplified rooftop solar: no feasibility study up to 10 kW, and DISCOM-funded network strengthening up to 5 kW. — [PIB, February 2024](https://www.pib.gov.in/PressReleaseIframePage.aspx?PRID=2008289); [Drishti IAS](https://www.drishtiias.com/daily-updates/daily-news-analysis/amendments-to-the-electricity-rights-of-consumers-rules-2020)

### Inferences
- Eskom proves the concept, cost-effectiveness and regulatory feasibility of "brownout instead of blackout" via smart meters. GridKavach shouldn't claim the idea of load limiting as new.
- Eskom's version is a flat amp cap that the household manages itself, rolled out first in affluent areas. GridKavach's possible novelty is in four places:
  - tiered essential loads (lights, fan, phone) guaranteed per home;
  - institutional priority (clinics);
  - a community-battery floor that keeps the limit alive even when the feeder is off;
  - deliberate targeting of low-income areas, where the South African evidence shows equity failures.
- The Eskom lessons (comms reliability, in-home display, SMS warnings) should be built in as design requirements. They also give a credible baseline: about 1 kW per meter and about 70% response.
- In India, the Consumer Rights Rules' reliability compensation gives DISCOMs a possible financial incentive to cut full outages. This is an inference; I didn't verify how compensation is enforced.

### Gaps
- I didn't research load limiting in Pakistan or Nigeria, Indian "load limiter" history, or City of Cape Town's own municipal load-limiting results.
- I found no Eskom data on household satisfaction or medical-equipment outcomes.

## Q3. Community energy storage models and fair-access dispatch

### Takeaway
Community batteries are established: Australia funded 400+, and India has TPDDL's CESS plus BRPL's 20 MW/40 MWh. Their "fairness" mechanisms are tariff-based (local-use network tariffs and retailer plans), not access-during-shortage rules. TPDDL's CESS already gives "backup to preferential consumers" during outages. That is a direct precedent for priority backup and should be acknowledged.

### Cited Findings
- Australia: in October 2022 the government committed A$200 million for 400 community batteries. A$171 million went via ARENA (at least 342 batteries) and the rest via DCCEEW. — [ANAO audit, Report No. 24 2025-26](https://www.anao.gov.au/work/performance-audit/community-batteries-household-solar-program)
- The program is expected to exceed 400 batteries (the minister announced "more than 420"). — [DCCEEW minister media release](https://minister.dcceew.gov.au/bowen/media-releases/more-420-community-batteries-lower-energy-costs-and-boost-reliability); [ARENA](https://arena.gov.au/news/arena-funds-national-community-battery-roll-out/)
- ANAO found evaluation "not adequately considered during planning". 66% of DCCEEW-funded projects extended end dates by an average of 40 weeks. — [ANAO audit PDF](https://www.anao.gov.au/sites/default/files/2026-03/Auditor-General_Report_2025-26_24.pdf)
- Ausgrid uses a community-battery "Local Use of System" tariff so nearby customers can use a shared battery like a home battery without the upfront cost. — [Ausgrid news](https://www.ausgrid.com.au/About-Us/News/Ausgrid-community-batteries-unlock-significant-savings-for-customers); [Ausgrid community batteries](https://www.ausgrid.com.au/transforming-the-grid/innovating-for-the-future/community-batteries)
- EnergyAustralia offers a retail community battery plan in NSW. — [EnergyAustralia](https://www.energyaustralia.com.au/about-us/media/news/energyaustralia-community-battery-energy-plan-offers-nsw-customers-lower-cost)
- Essential Energy has three approved battery tariffs, depending on size and LV/HV connection. The program aims to share local solar, including with households that have no panels. — [Essential Energy](https://www.essentialenergy.com.au/our-network/future-energy/community-batteries)
- Academic: deep reinforcement learning for community battery scheduling under load, PV and price uncertainty. — [arXiv 2312.03008](https://arxiv.org/pdf/2312.03008)
- **India:** TPDDL and Nexcharge set up India's first grid-connected Li-ion Community Energy Storage System (0.52 MWh, Rani Bagh substation, Delhi). It provides peak shaving, VAR compensation, DSM-based frequency response and "power backup to preferential consumers in case of grid outage". — [Mercom India](https://www.mercomindia.com/tata-power-nexcharge-battery-community-energy-storage); [Energetica India](https://www.energetica-india.net/news/nexcharge-tata-power-ddl-sets-up-indias-1st-grid-connected-li-ion-battery-based-cess-in-delhi)
- TPDDL also runs a 10 MWh BESS described as South Asia's first grid-scale storage at distribution-transformer level, plus DER integration programmes. — [Energy-Storage.News](https://www.energy-storage.news/delhi-government-minister-emphasises-need-for-battery-storage-at-visit-to-10mw-facility/); [TPDDL DER page](https://www.tatapower-ddl.com/corporate/smart-grid-index/DER)
- BRPL is installing a 20 MW/40 MWh BESS at the 33/11 kV Kilokari substation, with a GEAPP concessional loan covering 70% of cost (with IndiGrid). — [Saur Energy summary](https://www.saurenergy.com/solar-energy-blog/top-5-battery-energy-storage-projects-commissioned-in-india)
- ADB and Tata Power signed a deal on Delhi distribution grid enhancement with BESS. — [Tata Power press release](https://www.tatapower.com/news-and-media/media-releases/adb-tata-power-sign-deal-to-enhance-delhis-power-distribution-through-grid-enhancements-and-battery-energy-storage-system)
- Tata Power is deploying BESS to support critical infrastructure in Mumbai. — [Energy-Storage.News](https://www.energy-storage.news/tata-power-deploys-battery-storage-to-support-critical-infrastructure-in-mumbai-india/)

### Inferences
- Indian community storage so far is owned by the DISCOM and sits at the substation or DT. Australian community batteries are owned by networks, councils or retailers, and fairness comes through tariffs. I found no example in these sources of a battery owned by a community cooperative (RWA/SHG) in an Indian low-income area, with dispatch rules guaranteeing per-household essential energy. That combination is a plausible novelty claim, pending a deeper search.
- TPDDL's "preferential consumers" backup means clinic priority isn't new. GridKavach's version is transparent, rule-based, community-governed priority combined with per-home floors.

### Gaps
- I didn't research UK community batteries, US examples, or second-life battery pilots in India.
- I found no published "fair-access dispatch rules" for any community battery covering shortage or outage conditions.

## Q4. Digital permit-to-work / LOTO for utilities and automated back-feed / DER-aware switching safety

### Takeaway
ADMS platforms include switching management, validation and crew-clearance protocols. Industry guidance says crews must verify that all sources, including DG, are open before work. I found no product that automatically checks, before issuing a permit, that every downstream DER/inverter export is blocked. That is GridKavach's most distinctive claim, with a caveat: certified grid-tie inverters have an excellent anti-islanding record. Indian electrocution cases more often involve multiple supply sources or wrongful re-energisation.

### Cited Findings
- ADMS is characterised as prioritising safety, including switching sequences, protection coordination and crew clearance. — [Codibly: DERMS vs VPP vs ADMS](https://codibly.com/blog/articles/derms-vs-vpp)
- ADMS and DERMS need to be integrated because DERMS changes affect operations. DER alarms can pinpoint "unwanted backfeeds" by time and location. — [PulseGeek](https://pulsegeek.com/articles/derms-vs-adms-functions-overlaps-and-when-you-need-each/); [Smarter Grid Solutions](https://news.smartergridsolutions.com/debunking-four-common-misconceptions-about-adms-and-derms-capabilities)
- Utility clearance procedures exist in published form (e.g. Snohomish PUD clearance procedures). — [SnoPUD clearance procedures](https://switching.snopud.com/Content/E_Clearance_Procedures.htm)
- Industry safety guidance: after clearance, crews must test that lines are dead to confirm all sources, including distributed generation, are open. — [Incident Prevention: Solar backfeed safety](https://incident-prevention.com/blog/solar-backfeed-safety-on-distribution-and-secondary-circuits/)
- LLNL report on robust DERMS requirements. — [LLNL-TR-767077](https://www.osti.gov/servlets/purl/1544954)
- Schneider's Field Client mobile tool streamlines switching plans and claims crews save 35% of their time, with better productivity and safety. — [Schneider ADMS 3.10 documentation update](https://smartgrid.schneider-electric.com/s/blog-article/a05QO00000EiCVFYA3/adms-310-hf9-product-documentation-update)
- **India context:** grid-tied inverters in India must meet IS 16221 anti-islanding, which trips within about 200 ms. — [Heaven Green Energy explainer](https://www.heavengreenenergy.com/blog/solar-and-power-cuts-explained). This is a vendor blog; treat it as secondary.
- **Counter-evidence (be honest):** a 2026 SACE white paper says no lineworker has been killed or injured by backfeed from a UL 1741-certified grid-tied inverter. It quotes trade safety literature calling certified inverters "virtually 100 percent reliable". — [SACE plug-in solar white paper 2026](https://cleanenergy.org/wp-content/uploads/SACE_PluginSolar_WhitePaper_Final-V.7_2026.pdf)
- Indian lineman deaths are linked to permit and coordination failures:
  - Himachal: electrocuted after obtaining a shutdown permit when supply was "suddenly restored". — [The Tribune](https://www.tribuneindia.com/news/himachal/himachal-lineman-electrocuted-while-restoring-power-supply/)
  - Lucknow (September 2026): a feeder received power from a second source while assumed dead (Hindi report, "power supply from two sources"). — [Amar Ujala](https://amarujala.com/lucknow/power-supply-from-two-sources-lineman-dies-of-electrocution-lucknow-news-c-13-lko1070-1939768-2026-09-28)
  - Karnataka/BESCOM cases, with engineers booked in one instance. — [Deccan Herald (Kadur)](https://www.deccanherald.com/india/karnataka/lineman-electrocuted-kadur-2315178); [Deccan Herald (BESCOM engineers booked)](https://www.deccanherald.com/india/karnataka/bengaluru/bescom-engineers-booked-698771.html)

### Inferences
- Digital switching and clearance management is not new in ADMS. What I did not find is a permit workflow that interlocks with the DERs themselves: it detects back-feed sources and confirms inverter export is blocked by telemetry before releasing the permit. GridKavach can claim this, framed as "not found in surveyed products".
- Pitch framing matters. Leading with "rooftop solar kills linemen" is contestable given the certified-inverter record. A more defensible framing:
  - multi-source back-feed (second feeders, DG sets, non-compliant or tampered inverters, and home battery inverters wired wrongly);
  - wrongful re-energisation during permits, which the Indian incidents show.
  SafeLine tackles both by making the permit conditional on verified dead-ness from every known source.
- The "installer inverter-registry fee" doubles as the DER source inventory that the back-feed check depends on. That is an architectural link worth stating.

### Gaps
- I couldn't access detailed permit/safety-document functionality for Schneider, Siemens, GE Vernova or Hitachi ADMS, or for standalone PTW/LOTO software. They may include DER tagging, so the novelty claim should be phrased as "not found".
- I found no statistics on backfeed-caused lineman injuries in India specifically. No national Indian data was found.

## Q5. Academic work: critical-load prioritisation, rationing fairness, smart-meter curtailment, cold-load pickup

### Takeaway
There is a solid academic base for fair load shedding, "soft load shedding" via AMI quotas, and staged restoration under cold-load pickup. Most of it is algorithmic or simulated. GridKavach's contribution is a deployable, community-governed implementation, not a new theory.

### Cited Findings
- "Solving the fair electric load shedding problem in developing countries" models the Fair Load Shedding Problem as MIP. It uses utilitarian, egalitarian and envy-free welfare metrics and accounts for households' different needs. — [Springer, Autonomous Agents and Multi-Agent Systems](https://link.springer.com/article/10.1007/s10458-019-09428-8)
- "Algorithms for Fair Load Shedding in Developing Countries" proposes heuristics for pairwise and group-wise fairness. — [University of Bath portal](https://researchportal.bath.ac.uk/en/publications/algorithms-for-fair-load-shedding-in-developing-countries)
- "Fair Allocation Based Soft Load Shedding" (IntelliSys 2020) assigns per-household quotas instead of blackouts. It notes that AMI threshold metering makes this feasible by remotely limiting supply to a quota. — [arXiv 2002.00451](https://arxiv.org/abs/2002.00451)
- "Fair Division Algorithms for Electricity Distribution". — [arXiv 2205.14531](https://arxiv.org/pdf/2205.14531)
- "Fairly Wired: Towards Leximin-Optimal Division of Electricity" (2025). — [arXiv 2506.02193](https://arxiv.org/html/2506.02193)
- A smart retrofitted meter for developing countries, designed to implement load shedding as household-level allocation. — [ResearchGate](https://www.researchgate.net/publication/263053108_A_Smart_Retrofitted_Meter_for_Developing_Countries)
- "Power rationing in a long-term power shortage" quantifies trade-offs between maximising total power delivered and fairness. — [Energy Policy, ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0301421518304130)
- Cold-load pickup: after long outages, load diversity is lost, so staged restoration is preferred. A two-stage restoration method produces a sequence of switching that respects power-flow constraints. — [Poudel et al., IET Smart Grid 2021](https://doi.org/10.1049/stg2.12021); [arXiv 2004.07921](https://arxiv.org/pdf/2004.07921)
- Restoration optimisation that models cold-load pickup and interruption cost (2024). — [arXiv 2411.12353](https://arxiv.org/pdf/2411.12353)
- Feeder-level microgrid unit commitment that considers cold-load pickup. — [arXiv 2301.08350](https://arxiv.org/pdf/2301.08350)
- Critical load restoration using DERs. — [arXiv 1912.04535](https://arxiv.org/pdf/1912.04535)
- Patent prior art: "System and method for managing cold load pickup using demand response". — [US 8600573](https://image-ppubs.uspto.gov/dirsearch-public/print/downloadPdf/8600573)
- UK Project Smart ReStart: SMETS smart meters can stagger reconnection of controllable loads (EV chargers, heating) to reduce the restoration demand spike. This is direct prior art for "ColdStart". — [LCP: Project Smart ReStart](https://www.lcp.com/en/insights/blogs/project-smart-restart-how-smart-meters-can-help-to-strengthen-local-electricity-networks)
- FLISR uses smart-meter pings among its inputs to locate faults. — [IET Smart Grid / OSTI](https://www.osti.gov/pages/servlets/purl/1842201)
- Smart meters for partially observable outage detection (GAN-based). — [arXiv 1912.04992](https://arxiv.org/pdf/1912.04992)

### Inferences
- ColdStart has strong prior art in both the UK Smart ReStart project and the US patent. GridKavach should present it as applying staged, meter-level reconnection to Indian feeders, where the cold load is mostly fans, ACs and coolers. It shouldn't be presented as an invention.
- The fairness literature (egalitarian, leximin, envy-free) can be cited as the theory behind Flex's tiered rationing. That adds credibility rather than taking it away.

### Gaps
- I found no field trial results of fair or soft load shedding in India or Pakistan through these searches.

## Q6. Gaps: what combination is NOT offered for low-income Indian neighbourhoods?

### Takeaway
No surveyed source combines all of the following for a grid-connected low-income Indian urban feeder:
- community (RWA/SHG) ownership of a shared battery;
- per-home tiered essential-load guarantees plus clinic priority, delivered through DISCOM smart meters;
- a permit-to-work that is interlocked with DER and back-feed sources;
- last-gasp localisation and staged cold-load restoration;
- an installer-registry revenue model.

Each part has prior art. The integration, the governance model and the target segment are the defensible novelty.

### Cited Findings
- Load limiting exists (Eskom), but it was piloted in affluent suburbs. Poorer, dense areas got harsher "load reduction". — [SAGEN PDF](https://www.cityenergy.org.za/wp-content/uploads/2025/03/Eskom-Load-limiting-pilot.pdf); [Daily Maverick](https://www.dailymaverick.co.za/article/2025-11-10-soweto-residents-decry-ongoing-power-cuts-under-eskoms-load-reduction-programme/)
- Indian community storage is DISCOM-owned with "preferential consumer" backup. — [Mercom India](https://www.mercomindia.com/tata-power-nexcharge-battery-community-energy-storage)
- Group-wise load limiting exists in mini-grids (SparkMeter), but off-grid. — [Engineering for Change](https://www.engineeringforchange.org/solutions/product/sparkmeter/)
- Flexibility forecasting and LV co-pilots exist for DSOs (Siemens). — [Siemens](https://press.siemens.com/global/en/pressrelease/siemens-unveils-flexibility-software-increase-electricity-grid-capacity-moving-towards)
- Last-gasp OMS is standard. — [Renewable Energy World](https://www.renewableenergyworld.com/power-grid/outage-management/enhancing-outage-management-with-ami/)
- Staged smart-meter reconnection exists (UK Smart ReStart). — [LCP](https://www.lcp.com/en/insights/blogs/project-smart-restart-how-smart-meters-can-help-to-strengthen-local-electricity-networks)
- India's RDSS smart-meter rollout creates the hardware base GridKavach would run on, but deployment is behind the needed pace. — [Earth Energy Log](https://earthenergylog.com/articles/india-smart-meters-2026)

### Inferences
Defensible novelty claims, ranked from strongest to weakest:
1. **SafeLine DER-interlocked permit:** permit release is conditional on automated back-feed source discovery plus telemetry-confirmed inverter export block. I found no equivalent product. Frame the problem around multi-source back-feed and wrongful re-energisation, not only rooftop PV.
2. **Community-governed fair-access rules on a shared battery during shortages:** a per-home essential floor plus institutional priority, owned by an RWA/SHG cooperative under a DISCOM licence. I found no Indian or Australian precedent with this governance and shortage-time rule set.
3. **Tiered essential-load rationing for low-income urban India:** an extension of Eskom load limiting (flat 10 A) and the academic soft-load-shedding work. It adds appliance tiers, clinic priority, a battery-backed floor and low-income targeting. Novel in application and design, not in concept.
4. **The integrated bundle at feeder or neighbourhood scale:** Gap Radar, Flex, LastGasp and ColdStart together, priced and owned for community operators rather than enterprise DISCOM control rooms.

Claims GridKavach should not make:
- that last-gasp outage localisation is novel;
- that staged cold-load restoration via smart meters is novel;
- that load limiting instead of blackout is novel;
- that community batteries are novel;
- that DER flexibility forecasting is novel.

Risks to flag in the pitch, drawn from the evidence:
- comms reliability (Eskom's 70% response only came after fixing concentrators and SIMs);
- community resistance to smart meters (Gauteng/KZN, Eastern Cape);
- evaluation weaknesses in community battery programs (ANAO);
- the low base rate of certified-inverter backfeed injuries.

### Gaps
- I didn't do an Indian patent search on DER-interlocked permit-to-work or tiered rationing. A patent search (Indian Patent Office, Google Patents) is recommended before claiming formal novelty.
- I didn't check whether Indian regulators (CEA safety regulations, state commissions) already mandate any DER isolation step in shutdown permits.
- I didn't verify whether Indian regulation allows an RWA/SHG to own or operate a battery behind a DISCOM feeder (licensing or franchisee route).
