Base IG used for HL7-defined EHR-S product family implementation guides

https://build.fhir.org/ig/HL7/ehrs-base-ig/

## Running the scipt and IG publisher

### Convert scripts
```
@> (once) git config --global --add safe.directory /app
@> cd script
@> (once) npm install
@> node max2fhir.js
@> node max2plantuml.js > ../input/images-source/relationships.plantuml 
```

### To build IG
```
(optional)> ./_updatePublisher.sh
@> ./_genonce.sh
```

### Run unit-tests
```
@> curl -L https://github.com/hapifhir/org.hl7.fhir.core/releases/latest/download/validator_cli.jar -o validator_cli.jar
@> java -jar validator_cli.jar -version 5.0.0 input/examples/*.json -ig input/profiles -tx n/a
```
