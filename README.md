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

