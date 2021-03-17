<properties
	pageTitle="Running Vacuum or Optimize command on a partitioned Delta directory becomes no-op"
	description="Running Vacuum or Optimize command on a partitioned Delta directory becomes no-op"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="37dafe08-cdbd-4b4a-917f-93f7ec68237e"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Running Vacuum or Optimize command on a partitioned Delta directory becomes no-op

<!--issueDescription-->

Based on provided details and initial investigation, please find a summary of issue as below:

## **Problem**

Unable to optimize or vacuum a specific partition directory.	

## **Cause**

This can happen if you try to run optimize or vacuum command on a partition directory. For example, if you use a command like below to vacuum a specific partition directory, then it will not work, as running the operation against a specific partition directory is not supported. 

    vacuum my-table/foo=bar/date=20190101 RETAIN 0 hours

You can run any delta specific operation only on the root data directory.

## **Solution**
Running optimize or vacuum command against a specific partition directory is not supported. You should run a command like below to just vacuum on a partition directory:

    vacuum mytable where foo = 'bar' and date = '20190101' RETAIN 0 hours

## **Recommended Documents**

* [Vacuum a Delta table](https://docs.microsoft.com/azure/databricks/spark/latest/spark-sql/language-manual/vacuum#--vacuum-a-delta-table-delta-lake-on-azure-databricks)

<!--/issueDescription-->