# scaleio-docker-compose
Quickly deploy a test ScaleIO environment using multiple containers orchestrated by Docker Compose

Build is based on the manual procedure outlined in the ScaleIO Installation Guide https://www.emc.com/collateral/technicaldocument/emc-scaleio-installation-guide.pdf

# ScaleIO Installation Packages
The installation packages have been omitted from this repository and are available from 
https://support.emc.com/ . Once you have cloned this git repo please download the RPMs from EMC and add them under the 'RPMS' directory.

# Building the images
Docker  wont let you add files that are outside the context of the build (e.g. from ../../RPMS) so rather than trying to build the image from the directory that contains the Dockerfile, come up to the top level and use: 

```$ docker build . -f Dockerfiles/<component>/Dockerfile```

This avoids having to distribute and/or replicate the RPMS among the Dockerfile directories. 
  
  
