# Meeting Scenario Ontology

This repository contains an ontology for a meeting scenario, modeled using Protégé and hosted on GitHub Pages.

## SPARQL Query Interface
To run SPARQL queries on the ontology, visit the following URL:
[https://mahdialaaaldin.github.io/meeting-scenario-ontology/](https://mahdialaaaldin.github.io/meeting-scenario-ontology/)

### Example Queries
1. Retrieve all meetings managed by an electronic agenda:
   ```sparql
   PREFIX : <http://example.org/meeting-ontology#>

   SELECT ?meeting
   WHERE {
     ?agenda :manages ?meeting .
   }
