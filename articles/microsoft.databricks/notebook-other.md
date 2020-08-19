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

* **The cluster returns Cancelled in a Python notebook** - when you install a conflicting version of a library, such as ipython, ipywidgets, numpy, scipy, or pandas to the PYTHONPATH, then the REPL can break, causing all commands to return Cancelled after 30 seconds. This also breaks %sh, the notebook macro that lets you enter shell scripts in Python notebook cells. To solve this problem, do the following:

	* [Identify the conflicting library and uninstall it](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#identify-the-conflicting-library)
	* Install the correct version of the library in a notebook using [library utilities](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-utils#--library-utilities) or [pip3](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#option-1-install-in-a-notebook-using-pip3). Or with a [cluster-scoped init script](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled#option-2-install-using-a-cluster-scoped-init-script)

## **Recommended Documents**

* [Common Errors in Notebooks](https://kb.databricks.com/notebooks/common-errors-in-notebooks.html)

* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username). This is currently supported for:
	* Standard clusters in both Scala and Python
	* High Concurrency clusters in Python with Credential Passthrough **disabled**

* Databricks **Performance Tuning**:
	* [Azure Databricks Best Practices](https://github.com/Azure/AzureDatabricksBestPractices/blob/master/toc.md)
	* [Optimizing Apache Spark SQL Joins](https://databricks.com/session/optimizing-apache-spark-sql-joins)
	* [Correctness and Performance of Apache Spark SQL](https://databricks.com/session/a-framework-for-evaluating-the-performance-and-the-correctness-of-the-spark-sql-engine)
	* [Delta Engine Optimization](https://docs.microsoft.com/azure/databricks/delta/optimizations/)
