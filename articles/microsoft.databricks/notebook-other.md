<properties
	pageTitle="Diagnose and resolve issues with Notebook"
	description="Diagnose and resolve issues with Notebook"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677716"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d3320720-fa2f-4bf2-bd25-77fbca3033f8"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Notebook

## **Recommended Steps**

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform

* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.

* **The cluster returns Cancelled in a Python notebook** - when you install a conflicting version of a library, such as ipython, ipywidgets, numpy, scipy, or pandas to the PYTHONPATH, then the REPL can break, causing all commands to return Cancelled after 30 seconds. This also breaks %sh, the notebook macro that lets you enter shell scripts in Python notebook cells. To solve this problem, do the following:

	* [Identify the conflicting library and uninstall it](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#identify-the-conflicting-library)
	* Install the correct version of the library in a notebook using [library utilities](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-utils#--library-utilities) or [pip3](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#option-1-install-in-a-notebook-using-pip3) or with a [cluster-scoped init script](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#option-2-install-using-a-cluster-scoped-init-script)
	
* Getting error **java.io.EOFException** when handling huge data set in Spark R even with larger cluster - issue is caused by design since Spark R uses driver node specific framework resource. Resolution is to handle the pipeline with dividing data into smaller sets and conquer the results.

* Getting exception **py4j.security.Py4JSecurityException: … is not whitelisted** on High Concurrency cluster with Credential Passthrough enabled - this exception is thrown when you have accessed a method that Azure Databricks has not explicitly marked as safe for Azure Data Lake Storage credential passthrough clusters. In most cases, this means that the method could allow a user on a Azure Data Lake Storage credential passthrough cluster to access another user’s credentials. To resolve issue:
    - You can either disable Credential Passthrough for this HC cluster
    - Or use Standard cluster with Credential Passthrough enabled where single user access is allowed

## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [Common Errors in Notebooks](https://kb.databricks.com/notebooks/common-errors-in-notebooks.html)
* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username). This is currently supported for:
	* Standard clusters in both Scala and Python
	* High Concurrency clusters in Python with Credential Passthrough **disabled**

* Databricks **Performance Tuning**:
	* [Azure Databricks Best Practices](https://github.com/Azure/AzureDatabricksBestPractices/blob/master/toc.md)
	* [Optimizing Apache Spark SQL Joins](https://databricks.com/session/optimizing-apache-spark-sql-joins)
	* [Correctness and Performance of Apache Spark SQL](https://databricks.com/session/a-framework-for-evaluating-the-performance-and-the-correctness-of-the-spark-sql-engine)
	* [Delta Engine Optimization](https://docs.microsoft.com/azure/databricks/delta/optimizations/)
