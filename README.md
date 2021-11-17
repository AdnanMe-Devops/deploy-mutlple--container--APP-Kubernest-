# deploy-mutlple--container--APP-Kubernest-
Deploying a multi-container application to Azure Kubernetes Services

 configure CI/CD pipelines to automatically push a docker image to Kubernetes cluster abstracted by Azure Kubernetes Services (AKS).
pull a docker image from a public container registry, deploy your application to the docker image then push the image to a private container registry to get ready to be picked up by the release pipeline.



• Create Kubernetes cluster using Azure cli
• Create an Azure Container Registry (ACR), AKS and Azure SQL server
• Provision the Azure DevOps Team Project with a sample .NET Core application 
• Configure application and database deployment, using Continuous Deployment (CD) in the Azure DevOps using Azure Pipelines
• Initiate the build to automatically deploy the application to Docker image, push the image to private Azure registry.
• Automatically trigger release pipeline to pull the docker image and push it to Kubernetes cluster 

Main steps:
• Get the latest version of Kubernetes cluster so we can deploy it to Azure Kubernetes cluster
• Setting up the environment: Here we will configure three Azure resources namely Azure container registry, AKS, and Azure SQL server. 
• Configure Build and Release pipeline: we will manually map Azure resources such as AKS and Azure Container Registry to the build and release definitions
• Trigger a Build and deploy application: Trigger a build manually and upon completion, an automatic deployment of the application will be triggered. 
• Access the Kubernetes web dashboard in Azure Kubernetes Service (AKS): A short note on web dashboard in Azure Kubernetes that assists basic management operations.


Key Advantages of Azure Kubernetes Services (AKS)

• Hosts your Kubernetes environment. 
• Quick and easy to deploy
• Hosted control plane
• Manages containerized applications without container orchestration expertise.
• Eliminates burden of ongoing operations and maintenance by provisioning, upgrading, and scaling resources on demand while keeping the application online.
• Continuous build option that creates Docker images for faster deployments and reliability.
• Create resources and infrastructure inside the Azure Kubernetes cluster through Deployments and services manifest files.



This project uses a Dockerized ASP.NET Core web application - MyHealthClinic (MHC) and is deployed to a Kubernetes cluster running on Azure Kubernetes Service (AKS) using Azure DevOps.

There is a mhc-aks.yaml manifest file which consists of definitions to spin up Deployments and Services such as Load Balancer in the front and Redis Cache in the backend. The MHC application will be running in the mhc-front pod along with the Load Balancer.

The following tasks will be performed:

Create an Azure Container Registry (ACR), AKS and Azure SQL server

Provision the Azure DevOps Team Project with a .NET Core application using the Azure DevOps   .

Configure application and database deployment, using Continuous Deployment (CD) in the Azure DevOps

Initiate the build to automatically deploy the application
