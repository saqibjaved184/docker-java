## Overview 
Please run simple application (build & run from source). It should connect to the
database and expose health-check endpoint.


## Tasks
1. Create a Dockerfile for `Connection-app`
2. Provide a definition for `Connection-app` inside the file
   `docker-compose.yml`
3. Create ZIP file with all the files required to satisfy expectations. 


### Running the java application 
In order to run the application please follow instruction below:
Build (fatjar):
`gradle clean build`
Run:
`gradle bootRun` 

### Running postgresql
`docker-compose -f docker-compose.yml up`
Postgres should run on `localhost` login: `postgres` pass: `postgres`

## Expectations
After running `docker-compose -f docker-compose.yml up`, then the endpoint `http://localhost:8080/actuator/health` should return status 200.


1. Provide a mark down formatted file `architecture.md` with:
   a. Architectural patterns/recommendations on how to deploy this solution on
      AWS.
   b. Infrastructure Provisioning tools/systems recommended, explaining why that
      tool vs any other options.
2. Provide a folder `iac/` with infrastructure as code definitions (templates)
   for the architecture recommendations to deploy on AWS.
