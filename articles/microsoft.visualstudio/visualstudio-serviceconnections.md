<properties
	pageTitle="Service Connections"
	description="Issues related related to Azure classic service connection creation, permissions, user interface, different options available in UI or any other guidances related to service connection"
	infoBubbleText="Azure Pipelines issues related to service connection"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AzureServiceConnectionsIssues"
	supportTopicIds="32742293"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while using Service Connections

## **Recommended Steps**

* **The service connection in my Azure DevOps project is not authorized to allow deployment**

    In such cases, configure AAD as well and the new resource permissions for the AD user.

* **I'm facing a resource authorization error in my build**

    If you want to authorize any pipeline to use the service connection, go to **Azure Pipelines**, open the **Settings** page, select **Service connections**, and enable the setting **Allow all pipelines to use this connection** option for the connection.

* **I want to manually authorize a service connection for a specific pipeline**

    If you want to authorize a service connection for a specific pipeline, open the pipeline by selecting **Edit** and queue a build manually. You will see a resource authorization error and an **Authorize resources** action on the error. Choose this action to explicitly add the pipeline as an authorized user of the service connection. You can also authorize a specific pipeline manually by going to Service connections security > Pipeline permissions and add the specific pipeline you would like to authorize.


## **Recommended Documents**

* [Use a service connection in YAML](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-connection)
* [Use a service connection in Classic](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=classic#use-connection)
* [Pipeline permissions for service connections](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=classic#pipeline-permissions)
