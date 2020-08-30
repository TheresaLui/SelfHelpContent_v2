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

## **Recommended Documents**

* [Change Version of R (r-base)](https://kb.azuredatabricks.net/r/change-r-version.html)
* [Install rJava and RJDBC Libraries](https://kb.azuredatabricks.net/r/install-rjava-rjdbc-libraries.html)
* [Resolving Package or Namespace Loading Error](https://kb.azuredatabricks.net/r/namespace-onload.html)
* [How to Persist and Share Code in RStudio](https://kb.azuredatabricks.net/r/persist-share-code-rstudio.html)
* [Problem: Rendering an R Markdown File Containing sparklyr Code Fails](https://kb.azuredatabricks.net/r/rmarkdown-sparklyr-code.html)
* [Fix the Version of R Packages](https://kb.azuredatabricks.net/r/pin-r-packages.html)
* [How To Parallelize R Code with gapply](https://kb.azuredatabricks.net/r/sparkr-gapply.html)
* [How To Parallelize R Code with spark.lapply](https://kb.azuredatabricks.net/r/sparkr-lapply.html)
* Note that R is not supported with Table Access Control
