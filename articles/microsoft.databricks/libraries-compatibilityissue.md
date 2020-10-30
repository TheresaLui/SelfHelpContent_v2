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

> Microsoft Support helps isolate and resolve issues related to libraries installed and maintained by Azure Databricks. For third-party components, including libraries, Microsoft provides commercially reasonable support to help you further troubleshoot issues. Microsoft Support assists on a best-effort basis and might be able to resolve the issue. For open source connectors and projects hosted on Github, we recommend that you file issues on Github and follow up on them. Development efforts such as shading jars or building Python libraries are not supported through the standard support case submission process: they require a consulting engagement for faster resolution. Support might ask you to engage other channels for open-source technologies where you can find deep expertise for that technology. There are several community sites; two examples are the [Microsoft Q&A page for Azure Databricks](https://docs.microsoft.com/answers/topics/azure-databricks.html) and [Stack Overflow](https://stackoverflow.com/).

* [Libraries overview and Guidance](https://docs.microsoft.com/azure/databricks/libraries/)

## **Recommended Steps**

* Exception **py4j.security.Py4JSecurityException: … is not whitelisted** on High Concurrency cluster with Credential Passthrough enabled:
     * This exception is thrown when you have accessed a method that Azure Databricks has not explicitly marked as safe for Azure Data Lake Storage credential passthrough clusters. In most cases, this means that the method could allow a user on a Azure Data Lake Storage credential passthrough cluster to access another user’s credentials. To resolve issue:
          * You can either disable Credential Passthrough for this HC cluster
          * Or use Standard cluster with Credential Passthrough enabled where single user access is allowed

* Error: org.apache.spark.SparkException: Process List
     * Troubleshoot error as per article [Libraries fail with dependency exception](https://docs.microsoft.com/azure/databricks/kb/libraries/library-fail-dependency-exception)

* Error: ImportError: No module named XXX
     * Resolve the error as per steps in article [Library unavailability causing job failures](https://docs.microsoft.com/azure/databricks/kb/libraries/library-install-latency) 

* [How to: Correctly Update a Maven Library in Azure Databricks](https://docs.microsoft.com/azure/databricks/kb/libraries/maven-library-version-mgmt)

* [List of pre-installed libraries](https://docs.databricks.com/release-notes/runtime/5.4.html#installed-python-libraries)

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform

* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.
