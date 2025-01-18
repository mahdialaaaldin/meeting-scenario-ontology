# Meeting Scenario Ontology

This repository contains an ontology for a meeting scenario, modeled using Protégé and hosted on GitHub Pages.

## SPARQL Query Interface
To run SPARQL queries on the ontology, visit the following URL:
[https://mahdialaaaldin.github.io/meeting-scenario-ontology/](https://mahdialaaaldin.github.io/meeting-scenario-ontology/)

### Example Queries

#### Query 1: Retrieve all instances of `ex:Human`
```sparql
PREFIX ex: <http://example.org/>
SELECT ?human
WHERE {
  ?human a ex:Human .
}
```

#### Query 2: Retrieve the name of John Pappas
```sparql
PREFIX ex: <http://example.org/>
SELECT ?name
WHERE {
  ex:JohnPappas ex:hasName ?name .
}
```

#### Query 3: Retrieve the company John Pappas is an executive of
```sparql
PREFIX ex: <http://example.org/>
SELECT ?company
WHERE {
  ex:JohnPappas ex:isExecutiveOf ?company .
}
```
