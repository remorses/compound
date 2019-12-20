# Compound

Uses the `docker-compose` file to deploy the containers to google cloud run
Services can communicate with each other using the url `http://service-name`
To reach the deployed services just invoke `https://user.project.compound.website/service-name`
To cutomize the router behaviour use labels.


Features
- **easy routing**
- **automatic https**
- **infinitely scalable**
- **scale to zero**
- **highly concurrent**

Supported docker-compose features
- **build**, builds the image and pushes it automatically before deploying
- **image**, currently only images on `gcr.io`
- **command**, set the command of the container
- **entrypoint**, set container entrypoint
- **volumes**, rebuilds the image to include the volumes inside the container
- **environment**, set env variables
- **env_file**, set env variables


Unsupported features
- **ports**, services can only use http, you can call other services with `http://service-name`
- **stateful volumes**, volumes are immutable, used only to inject files inside the container
- **non http traffic**
- **networks**, the services share all one common network
- **everything else**
