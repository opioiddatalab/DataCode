# Opioid Descriptive Metrics
These descriptive metrics are intended to nudge epidemiology research and clinical pain treatment decisions to be more closely aligned. The list of metrics can be implemented in healthcare research databases with medication utilization data like insurance claims, prescription monitoring programs, and electronic health records. Some metrics rely on diagonsis or procedure codes (e.g., not available in state PMP data), and should be tailored to specific needs.

## Input data format
The data are expected to be in patient-level form, with one row corresponding to a single medical encounter per patient. Standard variable naming conventions are as follows:<br>

`varname` is drugname as string in any capitalization<br>
`varname` is quantity dispensed (or prescribed) as a continuous numeric<br>
`varname` is NDC as nominal numeric (string?)<br>
`varname` is date of dispensing in xxxx-xxx-xx format<br>
`varname` is unique patient identifier<br>
`varname_n` is dianosis code fields<br>
`varname_n` is procedure code fields<br>
<br>
(... to be added...)<br>

### General caveats
Some assumptions to keep in mind are as follows:
+ The drugs are being ingested as prescribed (e.g., not saved for future use after early discontinuation)
+ There are no external/unobserved sources of opioids (e.g., cash payment in insurance data)
+ Prescription information is being transmitted 100% accurately within the health data system
(See [here](https://github.com/opioiddatalab/WTD/blob/master/NOTEBOOK.md) for an exploration of possible ways to relax these assumptions.)

---

## Pharmacological practice
1. Predeominant opioid molecule
Which is the most commonly prescribed opioid molecule?
1. Opioid molecule variety
How many different opioid molecules are being used?
1. Time on opioid therapy (continuous, recent)
1. Time on opioid therapy (cumulative observed)
1. Titration period for new patients
1. Dose escalation for established patients
1. Number of previous refills of same (or similar) opioid
<br>
## Dichotomous flags
1=yes, 0=no
1. Any combination opioid (include two categories below) 
1. Any combination opioid with acetaminophen/paracetamol
1. Any combination opioid with aspirin
1. Any extended-release or long-acting opioid
1. Any extended-release opioid
1. Any immediate-release opioid
1. Any transmucosal immeditate-release fentanyl
1. Any patch
1. Any liquid
1. Any labeled abuse-deterrent properties
1. Breakthrough pain medicine provided (ER + IR)
1. Evidence of opioid rotation
<br>

## Co-prescriptions<br>
1. Any codeine cough supressant
1. Any benzodiazepine
1. Any z-drug sleep aid
1. Any barbiturates or anxiolytics
1. Buprenorphine (oral for addiction)
<br>

## Claims or EHR data-specific
Not available in PMP data. <br>

### Co-prescriptions<br>
1. Any anti-cholinergic
1. Any anti-depressants
1. Any CYP metabolic inhibitors
1. Anti-coagulants (warfarin)

### Diagnoses and Procedures
1. Hospice
1. Opioid use disorder diagnosis
1. Opioid abuse/dependence
1. Overdose (fatal)
1. Overdose (non-fatal)
1. Overdose (fatal or non-fatal)
1. Substance abuse treatment
1. Alcohol use (or abuse)
1. Any malignancy
1. Any malignancy excluding non melanoma skin cancers
1. Outpatient infusions
1. Any surgery

---
Initial list developed on December 2, 2019 by Bethany, Naoko, Shabbar, Brian, Nab, Alan, and Stephanie at UNC IPRC
