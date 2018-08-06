# activiti-keycloak

Keycloak wrapper for activiti IT - docker image used for Activiti tests and demos as a reference sso/idm implementation.

The dockerfile imports a realm named activiti from the json file so that the built image is configured with these realm settings.

A portOffset is also applied in the startup so that keycloak runs on port 8180 to avoid conflicts on 8080.

The configuration includes:

admin user for the springboot realm with password admin
testuser in group users with password password
hruser in group users and group hrusers and password password
client user for using admin client with password client

To start a container use docker run -p 8180:8180 activiti/activiti-keycloak
