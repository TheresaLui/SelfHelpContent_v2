<properties
  pagetitle="V2 - Pipeline Activities - Batch Service (Custom Activity)"
  description="V2 - Pipeline Activities - Batch Service (Custom Activity) Common Solutions"
  service=""
  resource=""
  ms.author="hemin"
  selfhelptype="Generic"
  supporttopicids="32637158"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="58f10bd5-ada3-484e-b2b6-a66d55a2226d"
  ownershipid="AzureData_DataFactory" />
# V2 - Pipeline Activities - Batch Service (Custom Activity)

## **Recommended Steps**

### **If you have a specific error code**

Please refer to [Data Factory Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#custom) to understand error code and see recommended actions.

### **If the issue is less obvious**

Data Factory custom activities runs your code logic in an Azure Batch pool of virtual machines. An activity failure can be the result of an error in activity configuration, batch pool, or custom code logic. Follow below troubleshooting steps to investigate custom activity failures:

* Was the failure caused by a transient error?
  * A transient error usually self-resolved with job retries or following activity runs. If the issue persists, likely you can observe the same failure cross multiple runs.
  * Check if there was any successful retry activity soon after the failure.
  * Check if there were error messages indicating a transient storage or network issue.

* Are your custom activity properties still valid?
  * Check Azure Batch linked service name, and if the linked service still exist.
  * Check the command line.
  * Check resource linked service and folder path, if resource files are used.

* Are the Azure Batch linked service properties still valid?
  * Check the batch account name and access key. Make sure they are up to date.
  * Check the batch URI and pool name.
	
* Are the resource files still accessible? 
  * This step is applicable only if resource linked service and folder path are used in your custom activity.
  * Use the same credential specified in the resource linked service, check if the folder path exists
  * Check if all the resource files exists under the folder path.

* Is your batch pool healthy and has enough compute resources?
  * Check Azure Batch event logs for errors that indicate node failures or resource allocation issues.
  * Make sure you have more than one node in your pool. 
  * Check and make sure all VM nodes are running on the most recent version of Azure Batch agent.
  * If the jobs your custom activity submits to Azure Batch seem stuck (not picked up by any node), likely the batch pool does not have enough resources, or some node has old Batch Agent installed.
  * Follow the [Azure Batch Best practices](https://docs.microsoft.com/azure/batch/best-practices#pool-lifetime-and-billing) to keep your compute node pool healthy.
	
* Can you run the batch job successfully from Azure CLI?
  * Log in to the Azure Batch account with the _az batch_ command, make sure the account name and authentication method are the same as your linked service uses.
  * Create a **job** with _az batch job create_ command, make sure to use the same batch pool your linked service uses.
  * Create a **task** with _az batch task create_ command, make sure to use the same command as your linked batch service uses, and specify _--resource-files_ as needed.
  * If running the batch job outside Data Factory also failed with similar symptoms, next step is to debug your custom code on the batch node.
  * For more information on Azure Batch CLI commands, please refer to the Azure Batch article - [Quickstart - Run your first Batch job with the Azure CLI](https://docs.microsoft.com/azure/batch/quick-create-cli).


## **Recommended Documents**

* [Data Factory Troubleshooting Guide - Custom Activity](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#custom)
* Custom activities documents
  * Permission of Custom Activity [_auto-user account_](https://docs.microsoft.com/azure/data-factory/transform-data-using-dotnet-custom-activity#custom-activity-permissions).
  * V2 Custom Activity versus V1 DotNet Activity [Comparison](https://docs.microsoft.com/azure/data-factory/transform-data-using-dotnet-custom-activity#compare-v2-v1).
  * Azure Batch Pool with [Auto-scaling](https://docs.microsoft.com/azure/data-factory/transform-data-using-dotnet-custom-activity#auto-scaling-of-azure-batch).
* [Azure Batch Best practices - pool lifetime](https://docs.microsoft.com/azure/batch/best-practices#pool-lifetime-and-billing)