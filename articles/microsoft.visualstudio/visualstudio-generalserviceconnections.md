<properties
  pagetitle="Azure pipelines issues while making use of Azure Service Connections&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,vimalt,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742313"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesazure"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Azure Service Connections

Use the following recommendations to resolve Azure pipeline issues when making Azure Service connections.

## **Recommended Steps**

* **Why are service endpoints automatically created when running YAML pipelines?**<br>
The service endpoints are created automatically because of AAD subscription auth specified in the pipelines. AAD auth in Pipelines is used for creating ARM service connection or AKS service connection. [Refer this document for more information](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops#create-an-azure-resource-manager-service-connection-using-automated-security).

* **Unable to delete the service connections**<br>
This situation is often encountered when trying to migrate to a new tenant. To resolve, go to the old tenant and delete the app registrations present and delete the [service connection via API](https://docs.microsoft.com/rest/api/azure/devops/serviceendpoint/endpoints/delete?view=azure-devops-rest-6.0).

* **Operation failed to create Service connection**<br>
When creating the service connection, [make sure that it is verified](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#create-a-service-connection)

* **Error: "Service Connection is unable to access the pipeline"**<br>
Make sure that you're using the correct service connection and that the tasks used in the pipeline can access the credentials defined in the secrets.  [Learn how to use a service connection](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection).

* **Failed to authorize the service connection resource for pipeline**<br>
Make sure that the appropriate service connection is selected in the pipeline and has the necessary [pipeline permissions](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#pipeline-permissions) are granted to access this service connection.

* **Service connection name cannot be read from variable in pipeline**<br>
By design, Azure DevOps does not allow Service Connection names to be used as pipeline variables. [Refer this document for more information](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection).

## **Recommended Documents**

* [Creating Service Endpoints](https://docs.microsoft.com/azure/devops/extend/develop/service-endpoints?view=azure-devops)
* [Azure Resource Manager Service Connection](https://docs.microsoft.com/azure/devops/pipelines/library/connect-to-azure?view=azure-devops)
* [Troubleshoot Azure Resource Manager service connections](https://docs.microsoft.com/azure/devops/pipelines/release/azure-rm-endpoint?view=azure-devops)
* [Service Connections](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops&tabs=yaml#use-a-service-connection)
* For service impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
