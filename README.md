# Run project

> Clone devops repository

`git clone git@github.com:andru1236/mock-devops.git`

> Clone backend and ui repository inside the devops repository

``` bash
cd mock-devops

# Clone backend
git clone git@github.com:andru1236/mock-backend.git

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
