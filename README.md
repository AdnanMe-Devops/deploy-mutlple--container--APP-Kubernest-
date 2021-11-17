# deploy-mutlple--container--APP-Kubernest-
Deploying a multi-container application to Azure Kubernetes Services
This project uses a Dockerized ASP.NET Core web application - MyHealthClinic (MHC) and is deployed to a Kubernetes cluster running on Azure Kubernetes Service (AKS) using Azure DevOps.

There is a mhc-aks.yaml manifest file which consists of definitions to spin up Deployments and Services such as Load Balancer in the front and Redis Cache in the backend. The MHC application will be running in the mhc-front pod along with the Load Balancer.

The following tasks will be performed:

Create an Azure Container Registry (ACR), AKS and Azure SQL server

Provision the Azure DevOps Team Project with a .NET Core application using the Azure DevOps  Generator .

Configure application and database deployment, using Continuous Deployment (CD) in the Azure DevOps

Initiate the build to automatically deploy the application
