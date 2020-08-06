<properties
	pageTitle="Diagnose and resolve execution issues"
	description="Diagnose and resolve execution issues"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677690"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="635b660f-911e-4568-aab6-82ca7126648b"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve execution issues

## **Recommended Documents**

* How to connect to data sources from Azure Databricks:
     * [Azure SQL database](https://docs.microsoft.com/azure/databricks/data/data-sources/sql-databases)
     * [Azure Data Lake Storage](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-datalake-gen2)
     * [Azure Blob Storage](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/azure-storage)
     * [Azure Cosmos DB](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/cosmosdb-connector)
     * [Azure Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-spark-connector)
     * [Azure SQL Data Warehouse](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/)
* [Troubleshooting Unresponsive Python Notebooks or Canceled Commands](https://docs.microsoft.com/azure/databricks/kb/notebooks/troubleshoot-cancel-command)
* Python library conflicts can result in cancelled commands. The Azure Databricks support organization sees conflicts most often with versions of ipython, numpy, scipy, and pandas : [Troubleshooting Steps](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#python-command-cancelled) 
* [Common Errors in Notebooks](https://docs.microsoft.com/azure/databricks/kb/notebooks/common-errors-in-notebooks)
* [Cannot Run Notebook Commands After Canceling Streaming Cell](https://docs.microsoft.com/azure/databricks/kb/notebooks/streaming-notebook-stuck)

* To [increase quota limits](https://docs.microsoft.com/azure/azure-supportability/per-vm-quota-requests), please follow the steps:

    * Go to [subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
    * Select the subscription that needs an increased quota
    * Select Usage + quotas
    * In the upper right corner, select Request increase
    * Fill in the forms for the type of quota you need to increase
