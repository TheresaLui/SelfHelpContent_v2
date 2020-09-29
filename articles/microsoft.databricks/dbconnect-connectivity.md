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

* Push the JAR to Databricks cluster directly using Databricks Connect instead of the UI:  

	1. Use the [REST API to post the JAR to the DBFS directly](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/dbfs#--put), or
	2. [Upload the JAR to DBFS programmatically](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/examples#--upload-a-big-file-into-dbfs)
	3. Use the [REST API to install the library to cluster](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries#--install)

## **Recommended Documents**

* [Databricks Connect](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect)
* [How to install the client?](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#step-1-install-the-client)
* [How to configure connection properties?](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#step-2-configure-connection-properties)
* [How to configure IDE or notebook server to use Databricks Connect?](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#set-up-your-ide-or-notebook-server)
* [Databricks Connect Troubleshooting](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect#troubleshooting)


