Clone this repo

Get the HL7 Validator 

https://confluence.hl7.org/display/FHIR/Using+the+FHIR+Validator


java -jar validator_cli.jar Composition/Composition-RichardSmith.xml -ig https://packages.simplifier.net/CareConnect.STU3.02.00.00/-/CareConnect.STU3.02.00.00-2.0.0.tgz -ig NHSDigitalSTU3/ -version 3.0 -tx n/a

java -jar validator_cli.jar Encounter/Encounter-RichardSmith.xml -ig https://packages.simplifier.net/CareConnect.STU3.02.00.00/-/CareConnect.STU3.02.00.00-2.0.0.tgz -ig NHSDigitalSTU3/ -version 3.0 -tx n/a

java -jar validator_cli.jar Bundle/TOC-RichardSmith.xml -ig NHSDigitalSTU3/ -ig 	https://packages.simplifier.net/CareConnect.STU3.02.00.00/-/CareConnect.STU3.02.00.00-2.0.0.tgz -version 3.0 -tx n/a


## Issues

- HL7 Validator does not currently support UK SNOMED CT. Workaround is to disable terminology validation
- Official StructureDefinitions contain snapshot. Workaround is to remove snapshots
- no IG Package. 
