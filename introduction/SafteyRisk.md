# Generic Safety Frameworks

#### detailed reading
- Failure Modes and Effects Analyses - [asq.org](asq.org)
- [ISO 26262-1:2018 - Functional Safety for Road Vehicles](https://www.iso.org/standard/68383.html)
- [ISO/PAS 21448 - Safety of the intended functionality for Road Vehicles](https://www.iso.org/standard/70939.html)
- [WISE Drive: Requirements Analysis Framework for Automated ](https://uwaterloo.ca/waterloo-intelligent-systems-engineering-lab/projects/wise-drive-requirements-analysis-framework-automated-driving)
- [ NHTSA - Automated Driving Systems: A Vision for Safety 2.0](https://www.nhtsa.gov/sites/nhtsa.dot.gov/files/documents/13069a-ads2.0_090617_v9a_tag.pdf)

#### Safety Reports
- [Waymo Safety Report](https://waymo.com/safety/)

- [GM Safety Report, 2018](https://www.gm.com/content/dam/company/docs/us/en/gmcom/gmsafetyreport.pdf)

- [Ford Safety Report, 2018](https://media.ford.com/content/dam/fordmedia/pdf/Ford_AV_LLC_FINAL_HR_2.pdf)

- [NTSB's Report on the 2018 Uber Crash](https://www.ntsb.gov/investigations/AccidentReports/Reports/HWY18MH010-prelim.pdf)

- [Uber Safety Report, 2018](https://uber.app.box.com/v/UberATGSafetyReport)

- [NHTSA Crash Statistics, 2015](https://crashstats.nhtsa.dot.gov/Api/Public/ViewPublication/812115)

- [How Many Miles of Driving Would It Take to Demonstrate Autonomous Vehicle Reliability?; Rand Corporation Report, 2016](https://www.rand.org/pubs/research_reports/RR1478.html)

## Terms

**harm** - physical harm to living thing

**risk** - probability that event occurs + the severity the event can cause

**safety** - process of avoiding unresonable risk of harm

**hazard** - unreasonabile risk of harm or treat to safety

## types of hazards
-mechanical, electrical, hardware, software, sensors, AI behaviour, human fallback, hacking

## NHTSA overview 
### Safety Framework
- take a system engineering aproach to safety
- autonomy design
- testing and crash mitigation
#### autonomy design
- well degined ODD 
- OEDR
- have a fallback
- follow traffic laws
- think about cyber threats
- HMI - displays status info to user
#### testing and crash mitigation
-testing
- crashworthiness
- post crash safety: i.e. turn off fuelpumps, alert emergency services, go to a safe "state"
- have a blackbox for data recording
- have consumer education

## Fault Trees
- preliminary analysis
- top down glow
- deductive analysis
- analyze failures that might occur
- boolean logic to combine probabilities
    - AND probability is multiplying, OR is adding them.
- too node is general failure
- each child node is a more specific grouping of failure

## FMEA
Gist is make a RPN (risk priority number) made of Severity * Occurance * Detectability
- bottum up process to identify all effect of fault
- failure more
- effects analysis
- FMEA
  - categorize failure mode by priority
    - how serious
    - how frequent
    - how easily can it be detected
  - multiply these componsent for risk score
  - higher is worse and should be addressed first
  - steps
    - 1. discuss with field experts
    - 2. list failure modes
    - 3. identify effects
    - 4. root cause
    - 5. prevention method
    - 6. RPN (risk priority number) made of Severity * Occurance * Detectability

### HAZOP (variation on FMEA)
- brainstorm process, needs
- uses guid words to trigger brainstorming
  - dont have to assign specific numbers
- used early in design process
- sufficient design information is available and not likely to change

# Autonomous/Automotive Safety Frameworks
## Functional Safety Standard (AKA FuSa) from ISO 26262
- defition: the absence of unreasonable risk from
malfunctioning behavior caused by failures of the hardware and software in a car,or unintended behaviors arising with respect to its intended design. 
- only concered about hardward/software hazards
- V-Shaped Flow
- left side
  - requirement spec
  - architecture design
  - unit design
- right side
  - system integration testing
  - softare integration testing
  - unit testing
- HARA (Hazard and Risk Assessment)
  - identify faults & scenarios, assess risks, define worst-case

## Safety of Intended Functionality (SOTIF) from ISOPAR 21448.1
- Failure due to performance limitation and misuse
  - i.e sensor limitation, algo failures, user misuse
- Designed for level 0-2 Autonomy.
- Extension of FuSa
- Employs Hara
