# BgLZ 3.1.0

# Available source systems:

## [ECare - Puur](ECare%20-%20Puur/)
## [SDB Groep](SDB%20Groep/)


## Supported requests

### Patient
```
GET [base]/Patient?_include=Patient:general-practitioner
```
### TreatmentDirective
```
GET [base]/Consent?category=http://snomed.info/sct|11291000146105
```
### AdvanceDirective
```
GET [base]/Consent?category=http://snomed.info/sct|11341000146107
```
### Problem
```
GET [base]/Condition
```
### AllergyIntolerance
```
GET [base]/AllergyIntolerance
```
### LaboratoryTestResult
```
GET [base]/Observation/$lastn?category=http://snomed.info/sct|275711006
    &_include=Observation:related-target
    &_include=Observation:specimen
```
### Procedure
```
GET [base]/Procedure
```
### CarePlan
```
GET [base]/CarePlan?_include=CarePlan:activity-goal:Goal
    &_include=CarePlan:activity-outcomereference:Observation
    &_include=CarePlan:activity-medicaldevice:DeviceUseStatement
    &_include:recurse=DeviceUseStatement:device:Device
```
### CareTeam
```
GET [base]/CareTeam?_include=CareTeam:participant
```