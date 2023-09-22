# Integrale Zwangerschapskaart Pilot ~64

# Available source systems:

## [Orfeus](Orfeus/)
## Onatal

## Supported search requests

### Patient
```
GET [base]/Patient
```
### EpisodeOfCare
```
GET [base]/EpisodeOfCare?type=http://snomed.info/sct|364320009{&status=active|finished}&_include=EpisodeOfCare:organization&_include=EpisodeOfCare:care-manager
```
### Condition
```
GET [base]/Condition?context=EpisodeOfCare/{record-id}
```
### Encounter
```
GET [base]/Encounter?episodeofcare={record-id}&_include=Encounter:practitioner
```
### Procedure
```
GET [base]/Procedure?context=EpisodeOfCare/{record-id}&_include=Procedure:performer&_include=Procedure:based-on
```
### Observation - context EoC
```
GET [base]/Observation?context=EpisodeOfCare/{record-id}
```
### Observation - context Encounter
```
GET [base]/Observation?context:Encounter.episodeofcare=EpisodeOfCare/{record-id}
```
