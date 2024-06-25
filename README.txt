This repo is to show how to deploy a dockerized flask app to acr and then to container apps via github actions.

1) Create resources by running this terraform script (https://github.com/btindol/containerapps-albumapi-python.git)
2) In this repo create sp  (   az ad sp create-for-rbac --name "myServicePrincipal" --role Contributor --scopes /subscriptions/{subscription-id}/resourceGroups/{resource-group-name} --sdk-auth
3) Take json output and make it azure secrets
4) make the github actions
5) push a change to this repo and then watch it launch



How to run locally:

docker build -t flask-albums-app .

docker run -p 8080:8080 flask-albums-app
