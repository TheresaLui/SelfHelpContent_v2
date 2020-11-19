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

Microsoft Support helps to isolate and resolve issues related to libraries installed and maintained by Azure Databricks. For third-party components, including libraries, Microsoft provides commercially reasonable support to help you further troubleshoot issues. Microsoft Support assists on a best-effort basis and might be able to resolve the issue. For open source connectors and projects hosted on Github, we recommend that you file issues on Github and follow up on them. Development efforts such as shading jars or building Python libraries are not supported through the standard support case submission process: they require a consulting engagement for faster resolution. 

Support might ask you to engage other channels for open-source technologies where you can find deep expertise for that technology. There are several community sites; two examples are the [Microsoft Q&A page for Azure Databricks](https://docs.microsoft.com/answers/topics/azure-databricks.html) and [Stack Overflow](https://stackoverflow.com/).

* [Libraries overview and Guidance](https://docs.microsoft.com/azure/databricks/libraries/)

* To make third-party or custom code available to notebooks and jobs running on your clusters, you can install a library. Libraries can be written in Python, Java, Scala, and R. You can upload Java, Scala, and Python libraries and point to external packages in PyPI, Maven, and CRAN repositories.

    * You can manage libraries using the [Libraries CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/libraries-cli) or the [Libraries API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries).
    * You can install libraries in three modes: [workspace](https://docs.microsoft.com/azure/databricks/libraries/workspace-libraries), [cluster-installed](https://docs.microsoft.com/azure/databricks/libraries/cluster-libraries), and [notebook-scoped](https://docs.microsoft.com/azure/databricks/libraries/notebooks-python-libraries).

* Push the JAR to Databricks cluster directly using REST API and Databricks Connect:  

	**Step 1:** Use the REST API to post the JAR to the DBFS directly using [DBFS API Put](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/dbfs#--put). See [this example](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/examples#--upload-a-big-file-into-dbfs) of how to upload the JAR to DBFS programmatically.

	**Step 2:** Use the REST API to [install the library on cluster](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries#--install)

* The cluster returns **Cancelled** in a Python notebook
     * Follow this KB article to troubleshoot and resolve issue: [Cluster cancels Python command execution due to library conflict](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled)
	
## **Recommended Documents**

* [Install libraries on a cluster](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/libraries#--install)
* [Databricks Connect](https://docs.microsoft.com/azure/databricks/dev-tools/databricks-connect)
