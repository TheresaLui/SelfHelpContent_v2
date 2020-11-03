<properties
	pageTitle="Diagnose and resolve install issue through init script"
	description="Diagnose and resolve install issue through init script"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677698"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="bbefd82d-a16a-4b1f-b71e-eda86a206021"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve install issue through init script

## **Recoomended Steps**

* To make third-party or custom code available to notebooks and jobs running on your clusters, you can install a library. Libraries can be written in Python, Java, Scala, and R. You can upload Java, Scala, and Python libraries and point to external packages in PyPI, Maven, and CRAN repositories.

    * You can manage libraries using the [Libraries CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/libraries-cli) or the [Libraries API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries).
    * You can install libraries in three modes: [workspace](https://docs.microsoft.com/azure/databricks/libraries/workspace-libraries), [cluster-installed](https://docs.microsoft.com/azure/databricks/libraries/cluster-libraries), and [notebook-scoped](https://docs.microsoft.com/azure/databricks/libraries/notebooks-python-libraries).
    
## **Recommended Documents**

* [How to install a library on a cluster](https://docs.databricks.com/user-guide/libraries.html#install-a-library-on-a-cluster)
