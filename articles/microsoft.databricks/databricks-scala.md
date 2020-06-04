<properties
	pageTitle="Databricks Scala Issues"
	description="Databricks Scala Issues"
	service="microsoft.Databricks"
	resource="workspaces"
	authors="kywe665"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32612207"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ff13f5b9-50ad-4aa9-a5e7-262ffa99b28d"
	ownershipId="AzureData_AzureDatabricks"
/> 

# Azure Databricks Scala

## **Recommended steps**

- If you are trying to execute Scala code make sure you are either running in a Scala notebook or you specify "%Scala" as the first line in the cell
- Scala case classes [should be defined](https://docs.databricks.com/spark/latest/faq/common-errors-in-notebooks.html) in a cell of it's own otherwise you may encounter java.lang.NoClassDefFoundError: Could not initialize class line

## **Recommended documents**

1. [7 Tips to Debug Apache Spark Code Faster with Databricks](https://databricks.com/blog/2016/10/18/7-tips-to-debug-apache-spark-code-faster-with-databricks.html)
2. [Understanding your Apache Spark Application Through Visualization](https://databricks.com/blog/2015/06/22/understanding-your-spark-application-through-visualization.html)
3. [Databricks Scala DataFrames](https://docs.azuredatabricks.net/spark/latest/dataframes-datasets/introduction-to-dataframes-scala.html#dataframes-scala)
