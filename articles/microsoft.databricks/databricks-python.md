<properties
	pageTitle="Databricks Python Issues"
	description="Databricks Python Issues"
	service="microsoft.Databricks"
	resource="workspaces"
	authors="kywe665"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32612206"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2e802a04-972d-4944-8005-3c155c8baec1"
	ownershipId="AzureData_AzureDatabricks"
/> 

# Azure Databricks Python

## **Recommended steps**

- If you are trying to execute Python code make sure you are either running in a python notebook or you specify "%py" as the first line in the cell
- You cannot use both Python 2 and 3 in the same cluster since it is a cluster wide setting and not applied per notebook
- Databricks Runtime for Python is not an Anaconda distribution. If you want to install an Anaconda distribution on your cluster, follow [this guide](https://docs.azuredatabricks.net/user-guide/faq/anaconda-environment.html)

## **Recommended documents**

1. [Azure Databricks Python Clusters](https://docs.azuredatabricks.net/user-guide/clusters/python3.html)
2. [Databricks Library management](https://docs.databricks.com/user-guide/libraries.html)
3. [Databricks Python DataFrames](https://docs.azuredatabricks.net/spark/latest/dataframes-datasets/introduction-to-dataframes-python.html#dataframes-python)
