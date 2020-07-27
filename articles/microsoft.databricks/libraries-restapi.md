<properties
	pageTitle="Diagnose and resolve install issue through Rest API"
	description="Diagnose and resolve install issue through Rest API"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677699"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="98407fcd-0076-4c72-80a1-0aa58be664a7"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve install issue through Rest API

* Push the JAR to Databricks cluster directly using REST API and Databricks Connect:  

	**Step 1:** Use the REST API to post the JAR to the DBFS directly using [DBFS API Put](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/dbfs#--put) (this is an example on how to [upload the JAR to DBFS programmatically](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/examples#--upload-a-big-file-into-dbfs))

	**Step 2:** Use the REST API to [install the library on cluster](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries#--install)
	
## **Recommended Documents**

* [Install libraries on a cluster](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries#--install)
* [Databricks Connect](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect)
