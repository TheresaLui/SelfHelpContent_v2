<properties
  pagetitle="Azure pipelines issues while making use of Docker and Kubernetes service connections&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742309"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="dockerandkubernetesserviceconnections"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Docker and Kubernetes service connections

## **Recommended Steps**

* **I want to close all public access to Azure Container Registry and Azure Key Vault excluding Azure DevOps. What are the Azure DevOps's Public IP addresses?**
  - See the [list of IP ranges](https://docs.microsoft.com/azure/devops/organizations/security/allow-list-ip-url?view=azure-devops#ip-addresses-and-range-restrictions). You can also use [Self-Hosted Agents](https://docs.microsoft.com/azure/devops/pipelines/agents/v2-windows?view=azure-devops) to carry out this.

* **I received the error message, "The service connection does not exist or has not been authorized for use"**
  - This occurs because the service connection was either unauthorized or deleted. In such cases, authorize the service connection or [create a new one](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#create-a-service-connection).

* **How do I make use of docker Build & push image tasks in my YAML files in order to create a pipeline**
  - See [build and push](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/docker?view=azure-devops#build-and-push), which contains the YAML snippet to include in your pipeline.
    
* **I have an existing service connection and when trying to connect to the Azure Container Registry, it says no service connections exist**
  - This is because the release pipeline does not see the **Service Connection Endpoint** when adding an ACR artifact. The pipeline tasks will filter on **AZURE RM** for the Service Connection Endpoints. Therefore, use a [Service Connection Endpoint for Azure RM](https://docs.microsoft.com/azure/devops/extend/develop/service-endpoints?view=azure-devops).

* **Unable to modify name of docker registry service connection shared in another project, even though I have admin level access across all service connections**
  - In such cases, change the access level to **Basic** and you'll be able to rename the service connection of the docker registry.

## **Recommended Documents**

* [Troubleshoot Azure Resource Manager service connections](https://github.com/MicrosoftDocs/azure-devops-docs/blob/master/docs/pipelines/release/azure-rm-endpoint.md)
* [Build and push Docker images](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/docker?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
