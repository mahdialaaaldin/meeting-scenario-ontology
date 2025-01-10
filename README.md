# Meeting Scenario Ontology

This repository contains an ontology for a meeting scenario, modeled using Protégé and hosted on GitHub Pages.

## SPARQL Query Interface
To run SPARQL queries on the ontology, visit the following URL:
[https://mahdialaaaldin.github.io/meeting-scenario-ontology/](https://mahdialaaaldin.github.io/meeting-scenario-ontology/)

### Example Queries
### Query 1: Get all people working for a specific organization
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?person
WHERE {
  ?person :worksFor :ConstructionCompany .
}
```

### Query 2: Get all projects a specific person is involved in
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?project
WHERE {
  :JohnPappas :involvedIn ?project .
}
```

### Query 3: Get all meetings and their associated profiles
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?meeting ?date ?hour ?place
WHERE {
  ?meeting :hasProfile ?profile .
  ?profile :hasDate ?date .
  ?profile :hasHour ?hour .
  ?profile :hasPlace ?place .
}
```

### Query 4: Get all organizations and the people working for them
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?organization ?person
WHERE {
  ?person :worksFor ?organization .
}
```

### Query 5: Get the profiles of meetings managed by a specific agenda
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?meeting ?profile ?date ?hour ?place
WHERE {
  :Agenda :manages ?meeting .
  ?meeting :hasProfile ?profile .
  ?profile :hasDate ?date .
  ?profile :hasHour ?hour .
  ?profile :hasPlace ?place .
}
```

### Query 6: Get all people involved in any project
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?person
WHERE {
  ?person :involvedIn ?project .
}
```

### Query 7: Get the date and time of a meeting based on a specific project
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?date ?hour
WHERE {
  ?meeting :hasProfile ?profile .
  ?profile :hasDate ?date .
  ?profile :hasHour ?hour .
  ?meeting :hasProfile :ProjectXMeetingProfile .
}
```

### Query 8: Get all meetings for a specific project
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?meeting
WHERE {
  ?agenda :manages ?meeting .
  ?meeting :hasProfile ?profile .
  ?profile :hasDate ?date .
  ?project :hasProfile ?profile .
}
```

### Query 9: Get the place where a meeting is held
```sparql
PREFIX : <http://example.org/meeting-ontology#>
SELECT ?meeting ?place
WHERE {
  ?meeting :hasProfile ?profile .
  ?profile :hasPlace ?place .
}
```

