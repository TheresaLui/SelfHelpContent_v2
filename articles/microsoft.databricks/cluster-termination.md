<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster termination"
	description="Diagnose and resolve issues with Databricks cluster termination"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32784351"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b693e759-430f-4b6b-b47d-cfc21029d2aa"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster termination

## **Recommended Steps**

> Check [Azure Databricks status page](https://status.azuredatabricks.net/) for current status by region. We highly recommend subscribing for updates on this page, which will automatically notify you of future status changes.

* **By design, clusters which are idle for 30 days will be automatically deleted.** To prevent this deletion after 30 days idle time in the future, make sure to [Pin the cluster](https://docs.microsoft.com//azure/databricks/clusters/clusters-manage#--pin-a-cluster)
    
* [How to set Automatic termination](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#automatic-termination) 

 * For details on who deleted the cluster, please check [cluster event log](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#--cluster-event-logs)
