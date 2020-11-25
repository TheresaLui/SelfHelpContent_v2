<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation failure due to failed library installation"
	description="Diagnose and resolve issues with Databricks cluster creation failure due to failed library installation"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677679"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b508ffff-e283-4073-ad31-0d3aeff428bd"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation failure due to failed library installation

## **Recommended Steps**

* To make third-party or custom code available to notebooks and jobs running on your clusters, you can install a library. Libraries can be written in Python, Java, Scala, and R. You can upload Java, Scala, and Python libraries and point to external packages in PyPI, Maven, and CRAN repositories.

    * You can manage libraries using the [Libraries CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/libraries-cli) or the [Libraries API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries).
    * You can install libraries in three modes: [workspace](https://docs.microsoft.com/azure/databricks/libraries/workspace-libraries), [cluster-installed](https://docs.microsoft.com/azure/databricks/libraries/cluster-libraries), and [notebook-scoped](https://docs.microsoft.com/azure/databricks/libraries/notebooks-python-libraries).
    
## **Recommended Documents**

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform

* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Library Unavailability Causing Job Failures](https://docs.microsoft.com/azure/databricks/kb/libraries/library-install-latency)
* [Cluster Cancels Python Command Execution due to Library Conflict](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled)
