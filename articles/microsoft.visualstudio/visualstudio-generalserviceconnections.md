<properties
	pageTitle="Azure Service Connections"
	description="Issues related to service connection creation, permissions, user interface, usage of the connection types or any other guidances related to service connection"
	infoBubbleText="Azure Pipelines issues related to Service Endpoints"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsPipelinesAzure"
	supportTopicIds="32742313"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Azure Service Connections

## **Recommended Steps**

Are you facing one of these common problems?

* Unsure why service endpoints are getting created automatically while running YAML pipelines: The service endpoints are created automatically because of AAD subscription auth specified in the pipelines. AAD auth in Pipelines is used for creating ARM service connection or AKS service connection.[Refer this document for more information](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops#create-an-azure-resource-manager-service-connection-using-automated-security).

* Unable to delete the service connections: This situation is often encountered when you are trying to migrate to a new tenant. In such scenarios, go to the old tenant and delete the app registrations present and delete the [service connection via API](https://docs.microsoft.com/rest/api/azure/devops/serviceendpoint/endpoints/delete?view=azure-devops-rest-6.0).

* Service connection creation operation failed: Ensure that the service connection is verified while creating it. [Follow these steps](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#create-a-service-connection).

* I'm facing an error which reads **Service Connection is unable to access the pipeline**: Ensure the correct service connection is being used and the tasks used in the pipeline is able to access the credentials defined in the secrets. [Refer the document on how to use a service connection](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection).
* Failed to authorize the service connection resource for pipeline: Make sure the appropriate service connection is selected in the pipeline and the necessary [pipeline permissions](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#pipeline-permissions) are granted to access this service connection.
* Service connection name cannot be read from variable in pipeline: By design, Azure DevOps does not allow to use the Service Connection names as pipeline variables. [Refer this document for more information](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection).

## **Recommended Documents**

* [Creating Service Endpoints](https://docs.microsoft.com/azure/devops/extend/develop/service-endpoints?view=azure-devops)
* [Azure Resource Manager Service Connection](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops)
* [Troubleshoot Azure Resource Manager service connections](https://docs.microsoft.com/azure/devops/pipelines/release/azure-rm-endpoint?view=azure-devops)
* [Service Connections](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection)
