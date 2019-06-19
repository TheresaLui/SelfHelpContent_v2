<properties
	pageTitle="Managed Instance - Storage limit was hit"
	description="Managed Instance - Storage limit was hit"
	infoBubbleText="Managed Instance was hitting storage limit. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vlads"
	authors="vladsMDCS"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_StorageLimitHit"
	selfHelpType="diagnostics"
	supportTopicIds="32637296,32637300,32637306,32637313"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	articleId="sqlmanagedinstance-perf-increase-storage-limit"
/>
# Managed Instance - Storage limit was hit

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named **<!--$ServerName-->ServerName<!--/$ServerName-->** on subscription **<!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId-->** and resource group **<!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup-->** was hitting the preconfigured maximum storage limit of *<!--$reserved_storage_gb-->reserved_storage_gb<!--/$reserved_storage_gb--> GB* between *<!--$min_time-->min_time<!--/$min_time-->* and *<!--$max_time-->max_time<!--/$max_time-->*.

In this state, insert, update, delete, and index maintenance queries or any other requests that require system or user database space expansion will fail immediately due to the insufficient space.
<!--/issueDescription-->

## **Recommended Steps**

To enable normal operation of your instance, please increase the storage limit from:

* [Azure Portal - <!--$ServerName-->ServerName<!--/$ServerName-->](https://portal.azure.com/#resource/subscriptions/<!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId-->/resourceGroups/<!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup-->/providers/Microsoft.Sql/managedInstances/<!--$ServerName-->ServerName<!--/$ServerName-->)

* [Az PowerShell - Managed Instance update](https://docs.microsoft.com/powershell/module/Az.Sql/Set-AzSqlInstance)

	Example (with the current values):

	<code>
		Set-AzSqlInstance
		-ResourceGroupName <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup-->
		-Name <!--$ServerName-->ServerName<!--/$ServerName-->
		-VCore <!--$virtual_core_count-->virtual_core_count<!--/$virtual_core_count-->
		-StorageSizeInGB <!--$reserved_storage_gb-->reserved_storage_gb<!--/$reserved_storage_gb-->
	</code>

* [Azure CLI - Managed Instance update](https://docs.microsoft.com/cli/azure/sql/mi#az-sql-mi-update)

	Example (with the current values)

	<code>
		az sql mi update
		--subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId-->
		--resource-group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup-->
		--name <!--$ServerName-->ServerName<!--/$ServerName-->
		--capacity <!--$virtual_core_count-->virtual_core_count<!--/$virtual_core_count-->
		--storage <!--$reserved_storage_gb-->reserved_storage_gb<!--/$reserved_storage_gb-->
	</code>

## **Recommended Documents**

* [Managed Instance resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits)
* [Managed Instance service tiers](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-service-tiers)
* [What to do if Azure SQL Managed Instance reaches the max storage limit?](https://stackoverflow.com/questions/54150468/what-to-do-if-azure-sql-managed-instance-reaches-the-max-storage-limit)
