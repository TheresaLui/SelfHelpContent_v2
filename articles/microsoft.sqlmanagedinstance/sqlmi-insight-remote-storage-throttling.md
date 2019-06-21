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
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	articleId="sqlmanagedinstance-perf-remote-storage-throttling"
/>

# Managed Instance - Remote storage throttling

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup-->  had degraded performance between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> due to remote storage throttling.

Performance limits given to us by the remote storage are given on a file tier basis. When we have a situation in which the amount of used performance is getting close to the performance limit, throttling happens.
<!--/issueDescription-->

## Recommended Steps

If you have free, unneeded storage space on your Managed Instance, you can get better performance by simply resizing your file. More information about storage performance best practices can be found [on this link](https://techcommunity.microsoft.com/t5/DataCAT/Storage-performance-best-practices-and-considerations-for-Azure/ba-p/305525).

To enlarge the log file, use the `MODIFY FILE` clause of the `ALTER DATABASE` statement, specifying the `SIZE` and `MAXSIZE` syntax. For more information, see [ALTER DATABASE (Transact-SQL) File and Filegroup options](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-file-and-filegroup-options?view=sql-server-2017).

In addition, here is the list of affected files which should be resized:  <!--$setFilePath-->setFilePath<!--/$setFilePath-->.