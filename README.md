# Mock system
This system allow to the QA, developers simulate the any component non functional like:
- Rest APIS
- SNMP Devices
- GraphQL server (Next iteration)
- RabbitMQ with queues
- Databases

This components are simulated in a given PORT .

## Features
- Mock real **API REST FULL**
    - Allow mock all HTTP Methods (GET, POST, PUT, DELETE)
    - Allow to create end points easier
    - Allow to mock query params
    - Allow to upload .json files as response
    - Create JSON responses through an editor
- Mock **Devices SNMP**
    - Simulate snmps files based on SNMP WALKs files
    - Fix SNMP WALKS file in a editor

In the next iteraion, you will be able to simulate in specific host: depende on the requirements of the user
## Dependencies
The system has 3 componentes:
- The simulator (The backend)
- The gateways (GraphQL, Rest API)
- The ui (React Application)

# Run system

> Clone devops repository (*This repository will orchestrate all the dependencies*)

`git clone git@github.com:andru1236/mock-devops.git`

> Clone backend, gateway, and ui repository inside the devops repository

``` bash
cd mock-devops

# Clone backend
git clone git@github.com:andru1236/mock-backend.git

# Clone the gateway
git clone git@github.com:andru1236/mock-gateway.git
# Clone ui
git clone git@github.com:andru1236/mock-ui.git

###########################
# CHANGE HOST   REQUIRED  #
###########################

cd mock-ui

nano .env
# Replace the REACT_APP_BACKEND for your ip
# Example
REACT_APP_BACKEND=10.2.9.10

cd ..

# run all as service
docker-compose up -d

# run with all stout in the console
docker-compose up --build
```
