# Run project

> Clone devops repository

`git clone git@gitlab.jalasoft.local:mock-api/devops-mock-api.git`

> Clone backend and ui repository inside the devops repository

``` bash
cd devops-mock-api

# Clone backend
git clone git@gitlab.jalasoft.local:mock-api/be-mock-api.git

# Clone ui
git clone git@gitlab.jalasoft.local:mock-api/ui-mock-api.git

###########################
# CHANGE HOST   REQUIRED  #
###########################

cd ui-api-mock

# Edit file /src/services/ApiServiceRest.ts
nano src/services/ApiServiceRest.ts

# line 8 change BASE_URL
# public readonly BASE_URL = 'your_ip:5000/api/v1';
# EXAMPLE:
public readonly BASE_URL = 'http://10.30.128.56:5000/api/v1';

# up all stack 
docker-compose up --build

# run as daemon (optional)
docker-compose -up -d
```
