# Alloy Interview Test

Welcome and thanks for having accepted the invite to this assignment.

We have just received a request from the dev team to deploy an application they just developed to finally resolve the burning issue of whether there are more cat lovers or dog lovers at Causeway?

The dev team has provided us with the source code of the front-end web-app, worker and the Node.js web-app along with the architecture of the application. You are to deploy the application and test it based off of the requirements received.

The architecture of the application is shown in the `architecure.png`. The application is made up of a front-end web app in Python which lets a user vote between two options, a Redis cache which collects new votes, a .NET worker which consumes votes and stores them in the Postgres database backed by a storage volume and a Node.js web app which shows the results of the voting in real time.

We have been instructed that the database must have `postgres:15-alpine` version and have the following credentials passed through environment variables POSTGRES_USER: postgres, POSTGRES_PASSWORD: postgres. The cache must use redis based on alpine linux and have a storage attached to it to store the votes.

Along with this we also need a debug deployment based off of `Alpine Linux`. This debug deployment should be able to ssh into other containers running inside the cluster and run basic network debug commands against other deployments. 

### MUST HAVES ###
- Caching capabilities.
- Ability to cast and review votes.
- Ability to debug network issues in the application if any.

### NICE TO HAVE ###
- For security the databse should only accept Ingress from the cache and Egress should be blocked.
- The client should be able to handle a spike in traffic on demand.
