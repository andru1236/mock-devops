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

cd ui-mock-api

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
