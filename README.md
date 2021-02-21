### Sales Report API ###

Source Code Management Tool : GitHub
Pipeline Tool : Azure Pipelines

Steps to create Pipeline:
1. Integrate GitHub repository with Azure Pipelins
2. Create pipeline using the ASP.NET template
3. Add dockerfile for the creation of docker containers and pull image for .net setup from dockerhub
4. Add templates for container webapp creation
5. Add template for container registry
6. Add steps in azure-pipelines.yml for Build, Test, Azure Resource Group creation, Container Registry, Application Deployment
7. Trigger the pipeline for master or release branches

Process followed:
1. Branching strategy includes : Master branch and release/* branches
2. Deployment stage is : Staging
3. Only the changes committed in release branch should go to Staging Deployment stage and eventually to Prod stage after approval
4. Master branch can be used as a last working commit for rollback

Ideal process:
1. Branches : master, release/*, dev/*
2. Limit pull reguest merges for release/* and master branch for developers
3. dev/* branch commits can be deployed to development environment
4. Spinup database in a separate server or container as it needs to keep the data safe from deletion
5. Detect if there are any changes to the SQL folder of database and run the script only if condition is true


