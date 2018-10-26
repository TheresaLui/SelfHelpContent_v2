<properties
	pageTitle="Databricks Python Issues"
	description="Databricks Python Issues"
	service="microsoft.Databricks"
	resource="clusters"
	authors="kywe665"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32612206"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
/> 

# Azure Databricks Python

## **Recommended steps**

- If you are trying to execute python code make sure you are either running in a python notebook or you specify "%py" as the first line in the cell.
- You cannot use both Python 2 and 3 in the same cluster it is a cluster wide setting, not per notebook.
- Databricks Python runtime is not an Anaconda distribution. If you want to install an Anaconda distribution on your cluster, follow [this guide](https://docs.azuredatabricks.net/user-guide/faq/anaconda-environment.html).

## **Recommended documents**

1. [Azure Databricks Python Clusters](https://docs.azuredatabricks.net/user-guide/clusters/python3.html)
2. [Databricks Library management](https://docs.databricks.com/user-guide/libraries.html)
3. [Databricks Python DataFrames](https://docs.azuredatabricks.net/spark/latest/dataframes-datasets/introduction-to-dataframes-python.html#dataframes-python).
