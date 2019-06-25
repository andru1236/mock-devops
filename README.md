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

# up all stack 
docker-compose up --build

# run as daemon (optional)
docker-compose -up -d
```
