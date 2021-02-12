<properties
	pageTitle="Notebook-How to"
	description="Notebook-How to"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677695"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0075b4da-2221-4f08-b065-da82552eb64a"
	ownershipId="AzureData_AzureDatabricks"
/>

# Notebook-How to

## **Recommended Steps**

* Facing **timeout error** when running [notebook workflows](https://docs.microsoft.com/azure/databricks/notebooks/notebook-workflows) as command is taking long time to execute - resolution would be to increase the notebook workflow timeout set in parent notebook to a suitable number after benchmarking: 

    ```
    dbutils.notebook.run("LOCATION_OF_CALLEE_NOTEBOOK", timeout)
    ```
    Also, it would be good to add additional logging in the code to get an idea on execution progress. This would make troubleshooting easier since these are non Spark logic and we won't find anything in driver logs.
    
* The cluster returns **Cancelled** in a Python notebook
     * Follow this KB article to troubleshoot and resolve issue: [Cluster cancels Python command execution due to library conflict](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled)
    
## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [Problem: Notebook Autosave Fails Due to File Size Limits](https://docs.microsoft.com/azure/databricks/kb/notebooks/notebook-autosave)
* [How to Get the Full Path to the Current Notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-path)
* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username). This is currently supported for:
	
	* Standard clusters in both Scala and Python
	* High Concurrency clusters in Python with Credential Passthrough **disabled**
