<properties
	pageTitle="Managed Instance - Remote Storage throttling"
	description="Managed Instance - Remote Storage throttling"
	infoBubbleText="Managed Instance was facing performance degradation due to remote storage throttling. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="v-zlrade"
	authors="v-zlrade"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_RemoteStorageThrottling"
	selfHelpType="diagnostics"
	supportTopicIds="32637224,32637296"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-perf-remote-storage-throttling"
	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Remote storage throttling

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup-->  had degraded performance between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> due to remote storage throttling.

Performance limits given to us by the remote storage are given on a file tier basis. When we have a situation in which the amount of used performance is getting close to the performance limit, throttling happens.
<!--/issueDescription-->

## Recommended Steps

* To enable normal operation of your instance, you will need to increase the size of following files which are affected:

<!--$setFilePath-->setFilePath<!--/$setFilePath-->

* To increase the size of file, use the __MODIFY FILE__ clause of the __ALTER DATABASE__ statement, specifying the __SIZE__ syntax, as described in the following example:

  ```
  alter database database_name
         modify file (name='file_name', size = 300GB)
  ```

## **Recommended Documents**

* [ALTER DATABASE (Transact-SQL) File and Filegroup options](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-file-and-filegroup-options?view=sql-server-2017)
