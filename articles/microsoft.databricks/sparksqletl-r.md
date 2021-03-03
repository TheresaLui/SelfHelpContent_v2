<properties
	pageTitle="Diagnose and resolve issues with R"
	description="Diagnose and resolve issues with R"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677725"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c2398469-febb-48fb-ba0e-b11b32fbd44d"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with R

## **Recommended Steps**

* Getting error **java.io.EOFException** when handling huge data set in Spark R even with larger cluster - issue is caused by design since Spark R uses driver node specific framework resource. Resolution is to handle the pipeline with dividing data into smaller sets and conquer the results.

* **Symptom:** 
  
  When cancelling R command on DBR < 7.1 (using sparklyr library), all python notebooks sharing the same interactive cluster are cancelling as well. 

  **Cause:** 
  
  This is a known bug with the sparklyr library.

  **Solution:** 
  
  Current workaround is to apply the following configuration at notebook level:

  ```
  config <- spark_config()
  config$sparklyr.cancellable = F
  spark_connect(spark_config = config)
  ```
  While there is currently no cluster level workaround for DBR < 7.1, there is a permanent fix with DBR >= 7.1.

## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [Change Version of R (r-base)](https://docs.microsoft.com/azure/databricks/kb/r/change-r-version)
* [Install rJava and RJDBC Libraries](https://docs.microsoft.com/azure/databricks/kb/r/install-rjava-rjdbc-libraries)
* [Resolving Package or Namespace Loading Error](https://docs.microsoft.com/azure/databricks/kb/r/namespace-onload)
* [How to Persist and Share Code in RStudio](https://docs.microsoft.com/azure/databricks/kb/r/persist-share-code-rstudio)
* [Problem: Rendering an R Markdown File Containing sparklyr Code Fails](https://docs.microsoft.com/azure/databricks/kb/r/rmarkdown-sparklyr-code)
* [Fix the Version of R Packages](https://docs.microsoft.com/azure/databricks/kb/r/pin-r-packages)
* [How To Parallelize R Code with gapply](https://docs.microsoft.com/azure/databricks/kb/r/sparkr-gapply)
* [How To Parallelize R Code with spark.lapply](https://docs.microsoft.com/azure/databricks/kb/r/sparkr-lapply)
* Note that R is not supported with Table Access Control
