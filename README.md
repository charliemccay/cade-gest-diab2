# cade-gest-diab
This is a demo Resouces folder for the CADE2 pathway-based simulation tool

To run a simulation you need to mount the Resources folder in this project in the CADE2 Docker container.  Note that you need to provide the absolute path for your local copy of the Resources folder.  The following command would work for user charliemccay on a macos machine with the folder cloned into my home directory.

This Resources file assumes that you have a locally running FHIR server - this can be stood up using the following command:

docker run -it -p 8080:8080 smartonfhir/hapi:r3-empty

Once the FHIR server is running, you can then run the CADE container which will post the patients and observations to the FHIR server.

docker run -v /Users/charliemccay/cade-gest-diab2/Resources:/app/Resources ramseysys/cade2 start.py

The FHIR server can be stopped with ctrl-c.  When it is started again it will be empty.  This implementation of CADE uses UUIDs for the resource identifiers, so can be run multiple times without clashing identifiers - every time someone is born they are assumed to be a new person.

The BPMN models can be edited with the Camunda Modelling tool: https://camunda.com/download/modeler/
