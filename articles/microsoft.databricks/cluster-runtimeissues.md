<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster runtime"
	description="Diagnose and resolve issues with Databricks cluster runtime"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32784352"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c4fe59be-d31e-4adc-be76-540f9f6cbee2"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster runtime (DBR)


> **Check [Azure Databricks status page](https://status.azuredatabricks.net/) for current status by region. We highly recommend subscribing for updates on this page, which will automatically notify you of future status changes.**

## **Recommended Documents**

* [Supported Databricks runtime releases and support schedule](https://docs.microsoft.com/azure/databricks/release-notes/runtime/releases#--supported-databricks-runtime-releases-and-support-schedule)

* Compatibility Matrixes - See Databricks Runtime and Databricks Runtime ML versions and their respective Delta Lake API and MLflow versions:

     * [Delta Lake API compatibility matrix](https://docs.microsoft.com/azure/databricks/release-notes/runtime/releases#delta-lake-api-compatibility-matrix)
     * [MLflow compatibility matrix](https://docs.microsoft.com/azure/databricks/release-notes/runtime/releases#mlflow-compatibility-matrix)
     
* [Supported Databricks Light releases](https://docs.microsoft.com/azure/databricks/release-notes/runtime/releases#supported-databricks-light-releases)

* **Is is possible to restore a cluster?**
  
  If a cluster is deleted, it cannot be restored by design. Instead, a new cluster should be created.

