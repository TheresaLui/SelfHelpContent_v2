<properties
	pageTitle="Databricks R Issues"
	description="Databricks R Issues"
	service="microsoft.Databricks"
	resource="workspaces"
	authors="kywe665"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32612203"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="19cfe703-c6c1-4c58-99fa-6b75117a3176"
	ownershipId="AzureData_AzureDatabricks"
/> 

# Azure Databricks R

## **Recommended steps**

- If you are trying to execute R code, make sure you are either running in an R notebook or you specify "%R" as the first line in the cell
- If you have trouble installing an rJava or RJDBC package, see [this guide](https://docs.databricks.com/spark/latest/sparkr/tips/install-rjava-rjdbc-libraries.html)
- R execution is limited to a single-threaded runtime and memory of a single machine. Use [SparkR](https://databricks.com/blog/2015/06/09/announcing-sparkr-r-on-spark.html) to scale your jobs and maximize performance in Spark

## **Recommended documents**

1. [SparkR Overview](https://docs.databricks.com/spark/latest/sparkr/overview.html)
2. [SparklyR Overview](https://docs.databricks.com/spark/latest/sparkr/sparklyr.html)
