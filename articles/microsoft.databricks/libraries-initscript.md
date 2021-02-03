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

## **Recommended Steps**

* To make third-party or custom code available to notebooks and jobs running on your clusters, you can install a library. Libraries can be written in Python, Java, Scala, and R. You can upload Java, Scala, and Python libraries and point to external packages in PyPI, Maven, and CRAN repositories.

    * You can manage libraries using the [Libraries CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/libraries-cli) or the [Libraries API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries).
    * You can install libraries in three modes: [workspace](https://docs.microsoft.com/azure/databricks/libraries/workspace-libraries), [cluster-installed](https://docs.microsoft.com/azure/databricks/libraries/cluster-libraries), and [notebook-scoped](https://docs.microsoft.com/azure/databricks/libraries/notebooks-python-libraries).
    
* The cluster returns **Cancelled** in a Python notebook
     * Follow this KB article to troubleshoot and resolve issue: [Cluster cancels Python command execution due to library conflict](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled)
    
## **Recommended Documents**

## **Recommended Documents**

Microsoft Support helps to isolate and resolve issues related to libraries installed and maintained by Azure Databricks. For third-party components, including libraries, Microsoft provides commercially reasonable support to help you further troubleshoot issues. Microsoft Support assists on a best-effort basis and might be able to resolve the issue. For open source connectors and projects hosted on Github, we recommend that you file issues on Github and follow up on them. Development efforts such as shading jars or building Python libraries are not supported through the standard support case submission process: they require a consulting engagement for faster resolution. 

Support might ask you to engage other channels for open-source technologies where you can find deep expertise for that technology. There are several community sites; two examples are the [Microsoft Q&A page for Azure Databricks](https://docs.microsoft.com/answers/topics/azure-databricks.html) and [Stack Overflow](https://stackoverflow.com/).

* [Libraries overview and Guidance](https://docs.microsoft.com/azure/databricks/libraries/)

* [How to install a library on a cluster](https://docs.databricks.com/user-guide/libraries.html#install-a-library-on-a-cluster)
