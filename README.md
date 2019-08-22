# cade-gest-diab
This is a demo Resouces folder for the CADE2 pathway-based simulation tool

To run a simulation you need to mount the Resources folder in this project in the CADE2 Docker container.  Note that you need to provide the absolute path for your local copy of the Resources folder.  The following command would work for user charliemccay on a macos machine with the folder cloned into my home directory.

docker run -v /Users/charliemccay/cade-gest-diab/Resources:/app/Resources ramseysys/cade2 start.py
