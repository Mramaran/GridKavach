# Safety, Back-feed, Smart-Meter and FLISR Facts for the GridKavach Protection Layer (India)

Research date: 2026-10-01. Every figure has a URL. Items I could not verify are in the "Gaps" sections. Some figures come from search-engine snippets of official PDFs that I could not open in full; they are marked "(snippet)".

## Q1. How many people die from electrocution in India, and how many of them are linemen?

### Takeaway
NCRB counts about 12,000 to 13,000 electrocution deaths a year in India (12,492 in 2022). I found no national figure for linemen or utility workers. State data exists only in fragments: Tamil Nadu (35 gangman trainees killed from Mar 2021 to Nov 2022) and Goa (5 linesmen in 2023). Treat any "X linemen die every year in India" statement as unverified.

### Cited Findings
- NCRB ADSI 2022: electrocution deaths rose to **12,492 in 2022**. About 100,000 people died from electrocution in 2011–2020 (~11,000 a year, ~30+ a day) — [WION, citing NCRB](https://www.wionews.com/india-news/electrocution-fatalities-30-people-killed-every-day-in-india-says-ncrb-data-610035); NCRB ADSI 2022 report PDF: [ncrb.gov.in ADSI 2022](https://ncrb.gov.in/uploads/nationalcrimerecordsbureau/custom/adsiyearwise2022/1701611156012ADSI2022Publication2022.pdf)
- Newslaundry (Aug 2023): "Electrocution kills 12,500 a year" — [Newslaundry](https://www.newslaundry.com/2023/08/01/electrocution-kills-12500-a-year-but-indias-power-safety-problem-still-finds-little-media-space)
- NCRB ADSI 2023 (latest edition found): total accidental deaths **4,44,104 in 2023**, up from 4,30,504 in 2022 — [The Policy Edge](https://www.policyedge.in/p/ncrb-report-accidental-deaths-and); ADSI 2023 PDF: [ncrb.gov.in](https://www.ncrb.gov.in/uploads/files/1ADSIPublication-2023.pdf). A search snippet says electrocution was about 3.1% of accidental deaths in 2023, but I could not confirm the exact 2023 electrocution count from a primary page (snippet, unverified).
- Tamil Nadu (TANGEDCO): **35 gangman trainees electrocuted** between Mar 2021 (when the post was created; 9,600 trainees recruited) and Nov 2022. A union representative said trainees were put on all kinds of work, live lines included, because of field-staff shortages — [DT Next, 14 Nov 2022](https://www.dtnext.in/amp/tamilnadu/2022/11/14/shocked-and-left-to-die-2)
- Tamil Nadu: about 1,700 electrocution deaths in 2016–2021 (~340 a year). A 2022 study is said to show 35% of victims were TANGEDCO workers or electrical contractors (snippet; I did not find the primary study) — [search snippet via DT Next / spicylaw](https://spicylaw.com/death-due-to-electrocution-and-liability-of-tangedco-to-pay-compensation/)
- NHRC issued notices to Tamil Nadu officials over electrocution deaths of contract workers — [News On AIR](https://www.newsonair.gov.in/nhrc-issues-notices-to-tamil-nadu-officials-over-electrocution-deaths-of-contract-workers)
- Goa Electricity Department: **5 linesmen electrocuted in 2023** ("highest in recent times"), 3 line helpers in 2022, 1 each in 2019 and 2018 — [The Goan editorial, 20 Apr 2024](https://www.thegoan.net/editorial/electrocution-of-lineman-exposes-failures-of-electricity-department/112483.html)
- Cases where line staff were killed during a shutdown because the line was re-energised, which is a permit-to-work failure:
  - Himachal (HPSEB, Palampur): lineman killed while working "after obtaining a shutdown permit"; supply was "suddenly restored" — [The Tribune](https://www.tribuneindia.com/news/himachal/himachal-lineman-electrocuted-while-restoring-power-supply/)
  - Haryana: linesman Tejpal (42) had permission to shut off power, but it was allegedly switched on while he worked; FIR registered — [The Tribune](https://www.tribuneindia.com/news/haryana/linesman-dies-of-electrocution-fir-registered/)
  - Lucknow, UP (Sept 2026): lineman killed restoring supply, attributed to negligence — [Amar Ujala, 27 Sep 2026](https://amarujala.com/lucknow/lineman-loses-his-life-due-to-negligence-in-lucknow-he-had-climbed-pole-to-restore-power-for-consumers-2026-09-27)
  - UP Bijnor (2 Feb 2024, Lalit Kumar, 35), Kashmir Baramulla (12 Feb 2024), Srinagar (June 2023) — [British Safety Council India, 2024](https://www.britsafe.in/safety-management-news/2024/linemen-fatalities-a-shocking-situation)
  - Karnataka (BESCOM, HESCOM) lineman electrocutions — [Deccan Herald, BESCOM](https://www.deccanherald.com/amp/story/india%2Fkarnataka%2Fbengaluru%2Fbescom-lineman-electrocuted-2169238); [Deccan Herald, Kadur](https://www.deccanherald.com/india/karnataka/lineman-electrocuted-kadur-2315178)

### Inferences
- In the pitch, use "~12,500 electrocution deaths a year in India (NCRB 2022)" as the headline. Back it with state anecdotes (TN 35 trainees in about 20 months; Goa 5 in 2023). Do not quote a national lineman death total.
- Several reported deaths are re-energisation during a permitted shutdown. A digital permit-to-work with a feeder interlock (SafeLine) targets that failure mode directly.

### Gaps
- CEA's yearly electrical accident statistics (fatal, departmental vs non-departmental) did not come up in search. I could not verify a CEA national figure for utility employees.
- I found no MSEDCL, UPPCL or Karnataka-wide lineman death totals.
- I could not confirm the exact NCRB 2023 electrocution count.

## Q2. Do back-feeds from inverters, DG sets and rooftop solar actually kill linemen in India?

### Takeaway
Yes, but the evidence is anecdotal. I found one well-documented Indian case: Goa, April 2024, where a lineman was killed by reverse feed from a battery inverter at a gym. Media and safety bodies regularly name generators and inverters as a back-feed source. I found **no confirmed Indian death from grid-tied rooftop-solar islanding**.

### Cited Findings
- Goa (Bicholim, Housing Board), April 2024: lineman electrocuted during repair work. The cause is believed to be a "reverse power surge" from a **battery-backed inverter at a nearby gymnasium** — [The Goan, 20 Apr 2024](https://www.thegoan.net/editorial/electrocution-of-lineman-exposes-failures-of-electricity-department/112483.html)
- British Safety Council India names, among lineman fatality causes, current that "flows back into the wires from the user's end" from generators and inverters — [britsafe.in, 2024](https://www.britsafe.in/safety-management-news/2024/linemen-fatalities-a-shocking-situation)
- Karnataka (Hubballi, HESCOM): supply was disconnected for line-shifting work, yet current flowed into the pole, possibly fed back through a nearby transformer — [Deccan Herald](https://www.deccanherald.com/amp/story/india%2Fkarnataka%2Fworker-electrocuted-power-pole-hubballi-2019673)
- Industry explainer: on-grid rooftop inverters shut off within about 200 ms under IS 16221 anti-islanding (vendor blog, secondary) — [Heaven Green Energy](https://www.heavengreenenergy.com/blog/solar-and-power-cuts-explained)

### Inferences
- For solar, the honest pitch line is: "Rooftop PV is required to have anti-islanding, but uncertified or hybrid inverters, home UPS inverters with improper change-over, and DG sets without change-over switches remain back-feed sources." A back-feed interlock that checks the line is dead (voltage presence from DT or smart meters) before permit issue adds value no matter what the source is.

### Gaps
- I found no documented Indian anti-islanding failure of a certified grid-tied PV inverter.
- I found no statistics on how many lineman deaths are attributed to back-feed.

## Q3. What do the CEA regulations require on permit-to-work, earthing and DER anti-islanding?

### Takeaway
The CEA Safety Regulations 2023 require earthing and discharge before handling conductors, and keep earths on until the permit-to-work is returned. The CEA DG Connectivity Regulations 2013 (amended 2019) require DER to stop energising the circuit if it faults. They also bar DER from energising a de-energised circuit, require it to stop energising within **2 s** of an unintended island, and allow reconnection only after **60 s** of stable voltage and frequency.

### Cited Findings
- CEA (Measures relating to Safety and Electric Supply) Regulations, 2023, Gazette notification of June 2023 — [CEA Gazette PDF](https://cea.nic.in/wp-content/uploads/notification/2023/06/pdf_100_183_English.pdf). Provisions (from search snippets of the regulation text):
  - "Before any conductor or apparatus is handled, adequate precautions shall be taken, by earthing or other suitable means, to discharge electrically such conductor... and to prevent any conductor or apparatus from being accidentally or inadvertently electrically charged when persons are working thereon." (snippet)
  - Earthing rods stay connected to the isolated section "till all men and materials have been moved away to safe zone and permit to work is returned on completion of the work." (snippet)
  - Local earths may be removed for testing only when all personnel are in the safe zone and the Engineer or Supervisor is present. Earths must be re-fixed before anyone approaches the conductors again. (snippet)
  - Summary deck: [IRADE presentation on 2023 regulations](https://irade.org/website/wp-content/uploads/2024/07/Day-2_Rishika-sharan_-Safety-and-Electric-Supply-Regulations.pdf)
- CEA (Technical Standards for Connectivity of the Distributed Generation Resources) Regulations, 2013 (Notification 12/X/STD(CONN)/GM/CEA, dated 30.09.2013), First Amendment 2019 (dated 06.02.2019). The protection sub-regulation (6) requires DER operating in parallel to have functions for:
  - (a) over/under-voltage trip at >110% / <80%, clearing time up to 2 s
  - (b) over/under-frequency trip at 50.5 Hz / 47.5 Hz, clearing time up to 0.2 s
  - (c) "cease to energise the circuit to which it is connected in case of any fault in this circuit"
  - (d) a function "to prevent the distributed generation resource from energising a de-energised circuit", with reconnection only when voltage and frequency are within limits and "stable for at least sixty seconds"
  - (e) a function to prevent unintended islanding and "cease to energise the electricity system within two seconds of the formation of an unintended Island"
  - Source: [CBIP consolidated text of the 2013 regulations with 2019 amendment](https://www.cbip.org/cearegulations/CEA%20DATA/Connectivity/Connectivity%20Regulation/Con%20Coneectivity%20Regulations%202013.pdf); [CEA 2019 amendment page](https://cea.nic.in/regulations/central-electricity-authority-technical-standards-for-connectivity-of-the-distributed-generation-resources-amendment-regulations-2019/?lang=en)

### Inferences
- The regulations already require the permit, isolation and earthing workflow. The gap is enforcement and coordination, as the Himachal and Haryana re-energisation cases show. SafeLine can be positioned as **digitising the existing CEA 2023 permit-to-work duty**, not as a new requirement.
- The anti-islanding 2 s limit covers compliant DER only. It does not cover off-grid or home UPS inverters or DG sets, which are not "distributed generation resources operating in parallel".

### Gaps
- I did not confirm the exact regulation numbers in the CEA 2023 Safety Regulations for the permit-to-work clauses; I only had snippet-level text.
- I did not retrieve the 2023/2024 amendments, if any, to the DG connectivity regulations.

## Q4. How big is RDSS smart metering: target, installed count and budget?

### Takeaway
**Correct the "22+ crore" claim.** RDSS has sanctioned **20.33 crore** smart meters: 19.79 crore consumer, 52.53 lakh DT and 2.05 lakh feeder meters. As of **30 June 2026**, **5.73 crore** were installed under RDSS (7.24 crore nationally). The scheme outlay is **Rs 3,03,758 crore** (GBS Rs 97,631 crore). The sunset date has moved to **31 March 2028**.

### Cited Findings
- As of 30 Jun 2026: **7.24 crore** smart meters installed nationally (consumer + DT + feeder), of which **5.73 crore under RDSS**. Sanctioned under RDSS: **20.33 crore** (19.79 crore consumer, 52.53 lakh DT, 2.05 lakh feeder). RDSS sunset date: **31 Mar 2028**. Source: written parliamentary reply by MoS Power Shripad Naik, reported 6 Aug 2026 — [T&D India](https://www.tndindia.com/indias-smart-meter-population-at-7-24-crore-parliament/)
- PIB release "Progress on Smart Meter Installation under RDSS" (could not open, HTTP 403) — [PIB PRID 2222217](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2222217&reg=3&lang=2); an earlier PIB release reported 4.76 crore installed — [PIB PRID 2200456](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2200456&reg=3&lang=1)
- Around July 2025: 2.44 crore installed out of 20.33 crore sanctioned (snippet) — [Ministry of Power RS reply / T&D India](https://www.tndindia.com/over-20-crore-smart-meters-okayed-under-rdss-tn-gets-most/)
- RDSS launched July 2021, outlay **Rs 3,03,758 crore**, GBS **Rs 97,631 crore**. Smart-metering works worth **Rs 1,30,671 crore** were sanctioned for 45 DISCOMs in 28 States/UTs — [Ministry of Power, Rajya Sabha Starred Q 68, 2 Dec 2024](https://powermin.gov.in/sites/default/files/uploads/RS02122024_Eng.pdf); [PIB RDSS launch](https://www.pib.gov.in/PressReleaseIframePage.aspx?PRID=1897764&reg=48&lang=2)
- The deadline was extended by 2 years — [India Smart Grid Forum news](https://indiasmartgrid.org/news-detail/govt-extends-deadline-for-smart-meter-installation-by-2-years)

### Inferences
- About 28% of RDSS-sanctioned meters were installed by mid-2026 (5.73 / 20.33). That is still a base of tens of millions of meters capable of last-gasp, and growing.
- Use "~20 crore sanctioned, 7.2 crore installed nationally (June 2026)" rather than "22+ crore".

### Gaps
- The figure "22.23 crore" (which may be the national smart meter target) is not confirmed in any source I read.

## Q5. Do Indian smart-meter standards support "last gasp" power-fail events, and does any Indian utility use them?

### Takeaway
Yes. Indian smart-meter specifications based on IS 16444 and IS 15959 Part 2 require power OFF/ON event logging and unsolicited push notifications. DISCOM tender specs such as BSES require a last-gasp signal with timestamp, backed by a super-capacitor. Tata Power-DDL (Delhi) says it uses smart-meter last gasp, integrated with its DMS, for instant outage detection.

### Cited Findings
- BSES Rajdhani (BRPL) smart meter technical spec (NIT FK/PG/674): "Meters shall have provisions to provide last gasp signals through communication module in case of power failure"; "the endpoint shall send the power outage notification with time stamp"; "the meter shall have proper power backup (like a super capacitor)"; functional tests as per **IS 16444 Table 1** — [BRPL tender spec PDF](https://www.bsesdelhi.com/documents/55701/246879/BRPL_NIT_NO_FK_PG_674_2.pdf/b395ea5d-5c4d-5f8f-92cd-cd2a4371cddb) (snippet-level)
- Meters can push data and events "in an unsolicited manner" as per **clause 6 of IS 15959 (Part 2)**. Meters "shall detect power OFF if all phase voltages are absent" and record power-OFF and power-ON events — [BRPL spec](https://www.bsesdelhi.com/documents/55701/246879/BRPL_NIT_NO_FK_PG_674_2.pdf/b395ea5d-5c4d-5f8f-92cd-cd2a4371cddb); CEA smart meter spec (Feb 2020) URL now returns 404: [CEA staging link](https://cea.adgstaging.in/wp-content/uploads/2020/04/Tech.-Specification-of-Smart-Meters-1-Ph-and-3-Ph-Feb-2020.pdf)
- Tata Power-DDL uses the smart meter's "last gasp" communication during outages. Through integration with its distribution management system it can detect outages instantly, dispatch crews early and tell consumers the likely restoration time — [ESMAP presentation by Tata Power (Subhadip Raychaudhuri), 2022](https://www.esmap.org/sites/default/files/2022/Cape%20Town%20Utitlies/Presentations%20Day%202/6A%20-%20Subhadip%20Raychaudhuri%20-%20Tata%20Power.pdf) (snippet; full PDF returned 403)
- Background on last-gasp hardware design — [EDN](https://www.edn.com/when-the-power-fails-designing-for-a-smart-meters-last-gasp/)

### Inferences
- LastGasp fault localisation rests on a capability that is already required in Indian tender specs. The novelty is SCADA-side topology correlation (meter → DT → feeder section), not the meter feature.

### Gaps
- I did not verify the exact IS 15959 Part 2 event codes for power failure (e.g., Power OFF/ON event IDs 101/102). I could not open the standard text.
- I found no RDSS-wide data on how reliably last-gasp messages arrive over RF-mesh or cellular networks during feeder-wide outages.
- I found no BSES or EESL statement on operational outage detection from last gasp.

## Q6. Which Indian utilities run FLISR/ADMS, and how fast do they restore faults?

### Takeaway
Tata Power-DDL says it was the **first Indian utility to implement ADMS**, with an Automated Power Restoration System (FLISR) that locates faults, isolates them and restores supply automatically. I found no published restoration-time figure for underground cable faults in Indian cities.

### Cited Findings
- "Tata Power-DDL is the first utility in India to implement Advanced Distribution Management System". It is integrated with GIS and replaces the conventional SCADA-DMS-OMS — [Tata Power-DDL Smart Grid: Monitoring & Control](https://www.tatapower-ddl.com/corporate/smart-grid-index/monitoring-control); [Company profile](https://www.tatapower-ddl.com/corporate/our-company/company-profile)
- APRS "gets invoked automatically... uses signals received from the network to locate a fault... automatically executes a sequence of network switching to isolate the fault and restore power to the rest of the network". It enables restoration of most consumers "within the minimum possible time", with no numeric time given — [Tata Power-DDL](https://www.tatapower-ddl.com/corporate/smart-grid-index/monitoring-control)

### Gaps
- Not verified: BSES ADMS, Schneider EcoStruxure ADMS India deployments, IPDS/RDSS SCADA town counts, typical Indian UG cable fault restoration times. I ran out of search budget before reaching them; do not use specific figures for these without further sourcing.

## Q7. What does the literature say about cold-load pickup after long outages?

### Takeaway
IEEE PES PSRC (WG D1) documents that loss of diversity after outages, plus motor, transformer and capacitor inrush, can push restoration current well above normal peak. In one worked example, cold-load demand reaches **210% of normal load**. Diversity is fully lost once an outage exceeds the longest appliance cycle, for example 30 minutes. CLPU can cause unwanted relay operation (re-trips) on restoration. I found no India-specific study of AC-driven CLPU.

### Cited Findings
All from [IEEE PES Power System Relaying Committee, "Cold Load Pickup Issues", report of WG D1 to the Line Protection Subcommittee (chair Dean Miller)](https://www.pes-psrc.org/kb/report/075.pdf):
- Cold load pickup is a composite of inrush and loss of load diversity after sustained outages of "several minutes to several hours".
- "a group of appliances that each cycles once every 30 minutes would lose all diversity for any outage exceeding 30 minutes". CLPU recovery time grows until the outage duration exceeds the longest cycle time of connected equipment.
- Motor starting is about **5–8× running current**. Measured examples include 6.88×, 7.26× and 7.5× steady-state current, and a cold-load inrush of 62 A that was **7.75×** rated. Transformer magnetising inrush can reach about **12× rating**, and capacitor transients 10–20× normal load current.
- Table 4.0 (hypothetical winter residential circuit): with loss of diversity, the total cold-load pickup factor is **210%** of normal circuit load.
- As load factor on existing circuits rises, "the likelihood of unwanted protective relay operation during circuit restoration increases". In regions with heavy air conditioning, summer load builds through the day to an early-evening peak.
- Case study: a 9-hour outage (NW USA, Nov 2006) took about **4,000 s (1 h 6 min)** for feeder current to fall back to the pre-outage 150 A.
- Sympathetic tripping of healthy feeders from voltage-recovery inrush is also documented.
- Further reading: [Cold load pickup for air-conditioners (academia.edu)](https://www.academia.edu/34276530/COLD_LOAD_PICK_UP_FOR_AIR_CONDITIONERS); [OSTI: restoration strategy considering CLPU uncertainty](https://www.osti.gov/pages/biblio/1845016-restoration-strategy-active-distribution-systems-considering-endogenous-uncertainty-cold-load-pickup); [ResearchGate: CLPU management using remote control](https://www.researchgate.net/publication/282027583_A_Practical_and_Cost_Effective_Cold_Load_Pickup_Management_Using_Remote_Control)

### Inferences
- In India, ACs and refrigerators are cyclic, thermostat-controlled loads. After a summer outage of more than about 30 min, the same loss of diversity applies. Staged restoration (ColdStart) is the standard mitigation in the literature. Present it as applying established IEEE guidance, not as a new finding.

### Gaps
- I found no Indian utility report quantifying CLPU re-trips or summer AC cold-load multiples.

## Q8. Summary verdict on the pitch claims

### Takeaway
- "Linemen die from back-feed": **plausible, anecdotally supported** (Goa 2024 inverter case). Not quantified nationally.
- "Re-energisation during permitted shutdown kills linemen": **supported** by multiple news cases.
- "22+ crore smart meters": **correct it** to 20.33 crore sanctioned under RDSS, 7.24 crore installed nationally (5.73 crore under RDSS) as of 30 Jun 2026.
- "Smart meters support last gasp": **supported** by DISCOM specs (BSES) and Tata Power-DDL use.
- "CLPU causes re-trips": **supported** by IEEE PSRC. The India-specific version is unverified.

### Cited Findings
- See the sections above for sources.

### Inferences
- The strongest numbers for slides: 12,492 electrocution deaths (NCRB 2022); 35 TANGEDCO trainee deaths in about 20 months; 2 s anti-islanding limit (CEA 2013/2019); 20.33 crore sanctioned / 7.24 crore installed meters; Rs 3.04 lakh crore RDSS; CLPU 210% / motor inrush 5–8×.

### Gaps
- CEA accident statistics, ADMS deployments other than Tata Power-DDL, and city fault-restoration times all remain unverified.
