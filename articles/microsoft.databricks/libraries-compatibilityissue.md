<properties
	pageTitle="Diagnose and resolve library compatibility issues"
	description="Diagnose and resolve library compatibility issues"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677707"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="171610b6-aa2c-4b63-a017-65a5b58f7c88"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve library compatibility issues

Microsoft Support helps to isolate and resolve issues related to libraries installed and maintained by Azure Databricks. For third-party components, including libraries, Microsoft provides commercially reasonable support to help you further troubleshoot issues. Microsoft Support assists on a best-effort basis and might be able to resolve the issue. 

For open source connectors and projects hosted on Github, we recommend that you file issues on Github and follow up on them. Development efforts such as shading jars or building Python libraries are not supported through the standard support case submission process: they require a consulting engagement for faster resolution. 

Support might ask you to engage other channels for open-source technologies, where you can find deep expertise for that technology. There are several community sites. Two examples are the [Microsoft Q&A page for Azure Databricks](https://docs.microsoft.com/answers/topics/azure-databricks.html) and [Stack Overflow](https://stackoverflow.com/).

## **Recommended Steps**

* [Libraries overview and guidance](https://docs.microsoft.com/azure/databricks/libraries/)

* To make third-party or custom code available to notebooks and jobs running on your clusters, you can install a library. Libraries can be written in Python, Java, Scala, and R. You can upload Java, Scala, and Python libraries and point to external packages in PyPI, Maven, and CRAN repositories.

    * You can manage libraries using the [Libraries CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/libraries-cli) or the [Libraries API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries).
    * You can install libraries in three modes: [workspace](https://docs.microsoft.com/azure/databricks/libraries/workspace-libraries), [cluster-installed](https://docs.microsoft.com/azure/databricks/libraries/cluster-libraries), and [notebook-scoped](https://docs.microsoft.com/azure/databricks/libraries/notebooks-python-libraries).

* Exception **py4j.security.Py4JSecurityException: … is not whitelisted** on High Concurrency cluster with Credential Passthrough enabled:
  This exception is thrown when you have accessed a method that Azure Databricks has not explicitly marked as safe for Azure Data Lake Storage credential passthrough clusters. In most cases, this means that the method could allow a user on a Azure Data Lake Storage credential passthrough cluster to access another user’s credentials. To resolve this issue, you can do one of the following:
  * Disable Credential Passthrough for this HC cluster
  * Use Standard cluster with Credential Passthrough enabled where single user access is allowed

* Error: org.apache.spark.SparkException: Process List
     * Troubleshoot the error as indicated in [Libraries fail with dependency exception](https://docs.microsoft.com/azure/databricks/kb/libraries/library-fail-dependency-exception)

* Error: ImportError: No module named XXX
     * Resolve the error by following the steps in [Library unavailability causing job failures](https://docs.microsoft.com/azure/databricks/kb/libraries/library-install-latency) 
     
* The cluster returns **Cancelled** in a Python notebook
     * Follow this KB article to troubleshoot and resolve issue: [Cluster cancels Python command execution due to library conflict](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled)

## **Recommended Documents**
* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform
* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.
* [List of pre-installed libraries](https://docs.microsoft.com/azure/databricks/release-notes/runtime/7.2#installed-python-libraries)
* [How to: Correctly Update a Maven Library in Azure Databricks](https://docs.microsoft.com/azure/databricks/kb/libraries/maven-library-version-mgmt)

