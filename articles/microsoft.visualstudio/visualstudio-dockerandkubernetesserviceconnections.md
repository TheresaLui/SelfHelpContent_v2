<properties
	pageTitle="Docker & Containers"
	description="Issues related to docker, kubernetes service connection creation, permissions, user interface, different options available in UI or any other guidances related to service connection"
	infoBubbleText="Azure Pipelines issues related to Docker and Kubernetes service connections"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="DockerandKubernetesServiceConnections"
	supportTopicIds="32742309"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Docker and Kubernetes service connections

## **Recommended Steps**

Are you facing one of these common problems?

* **I want to close all public access to Azure Container Registry and Azure Key Vault excluding Azure Devops. What are the Azure Devops's Public ip addresses?**

    	The list of IP ranges are given [here](https://docs.microsoft.com/azure/devops/organizations/security/allow-list-ip-url?view=azure-devops#ip-addresses-and-range-restrictions). You can also make use of a [Self-Hosted Agents](https://docs.microsoft.com/azure/devops/pipelines/agents/v2-windows?view=azure-devops) to carry out this.

* **I encounter the error message which reads "The service connection does not exist or has not been authorized for use"**

	This occurs because the service connection was either unauthorized or was deleted. In such cases, authorize the service connection or [create a new one](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#create-a-service-connection).

* **How do I make use of docker Build & push image tasks in my YAML files inorder to create a pipeline**

    	[Refer this document](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/docker?view=azure-devops#build-and-push) which contains the YAML snippet to include in your pipeline.
    
* **I have an existing service connction and when trying to connect to the Azure Container Registry , it says no service connections exist**

   	 This is because the release pipeline does not see the **Service Connection Endpoint** when adding an ACR artifact. The pipeline tasks will filter on **AZURE RM** for the Service Connection Endpoints. Therefore, use a [Service Connection Endpoint for Azure RM](https://docs.microsoft.com/azure/devops/extend/develop/service-endpoints?view=azure-devops).

* **Unable to modify name of docker registry service connection shared in another project even though I have admin level access across all service connections**

	In such cases, change the access level to **Basic** and you will be able to rename the service connection of the docker registry.

    

## **Recommended Documents**

* [Troubleshoot Azure Resource Manager service connections](https://github.com/MicrosoftDocs/azure-devops-docs/blob/master/docs/pipelines/release/azure-rm-endpoint.md)
* [Build and push Docker images](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/docker?view=azure-devops)
