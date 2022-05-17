Clone this repo

Get the HL7 Validator 

https://confluence.hl7.org/display/FHIR/Using+the+FHIR+Validator

### Single Resource 
java -jar validator_cli.jar Composition/Composition-RichardSmith.xml -ig https://packages.simplifier.net/uk.nhsdigital.stu3.test/-/uk.nhsdigital.stu3.test-0.0.1-prerelease.tgz -version 3.0 -tx n/a

### Full Bundle

java -jar validator_cli.jar Bundle/TOC-RichardSmith.xml -ig https://packages.simplifier.net/uk.nhsdigital.stu3.test/-/uk.nhsdigital.stu3.test-0.0.1-prerelease.tgz -version 3.0 -tx n/a

## Issues

- HL7 Validator does not currently support UK SNOMED CT. Workaround is to disable terminology validation
- Official StructureDefinitions contain snapshot. Workaround is to remove snapshots
- no IG Package. 
- Extension https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1 is not allowed to be used in Encounters. Removed from examples.
- The bundle is difficult to navigate. E.g. an error like `Error @ Bundle.entry[17].resource.ofType(List).entry[0].item (line 1589, col12): Invalid Resource target type. Found Procedure, but expected one of ([])` Need to find the 17th resource and see what it is.

## Old versions of HL7 CLI

java -jar validator_cli.jar Composition/Composition-RichardSmith.xml -ig https://packages.simplifier.net/CareConnect.STU3.02.00.00/-/CareConnect.STU3.02.00.00-2.0.0.tgz -ig NHSDigitalSTU3/ -version 3.0 -tx n/a

java -jar validator_cli.jar Encounter/Encounter-RichardSmith.xml -ig https://packages.simplifier.net/CareConnect.STU3.02.00.00/-/CareConnect.STU3.02.00.00-2.0.0.tgz -ig NHSDigitalSTU3/ -version 3.0 -tx n/a

java -jar validator_cli.jar Bundle/TOC-RichardSmith.xml -ig NHSDigitalSTU3/ -ig 	https://packages.simplifier.net/CareConnect.STU3.02.00.00/-/CareConnect.STU3.02.00.00-2.0.0.tgz -version 3.0 -tx n/a
