<properties
	pageTitle="Diagnose and resolve issues related to connectivity with IDE"
	description="Diagnose and resolve issues related to connectivity with IDE"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677677"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2848290e-5aaa-477e-b3cf-f8c58cb4f5b6"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues related to connectivity with IDE

## **Recommended Steps**

* Push the JAR to Databricks cluster directly using Databricks Connect instead of the UI:  

	- Use the [REST API to post the JAR to the DBFS directly](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/dbfs#--put), or
	- [Upload the JAR to DBFS programmatically](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/examples#--upload-a-big-file-into-dbfs)
	- Use the [REST API to install the library to cluster](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries#--install)

## **Recommended Documents**

* [Databricks Connect](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect)
* [How to setup the client?](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#set-up-client)
* [How to setup IDE or notebook server to use Databricks Connect?](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#set-up-your-ide-or-notebook-server)
* [Databricks Connect Troubleshooting](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#troubleshooting)
* [Limitations](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#limitations)


