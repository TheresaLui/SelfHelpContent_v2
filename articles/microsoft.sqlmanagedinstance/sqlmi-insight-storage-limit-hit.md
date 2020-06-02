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
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-perf-increase-storage-limit"
	ownershipId="AzureData_AzureSQLMI"
/>
# Managed Instance - Storage limit was hit

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> was hitting the preconfigured maximum storage limit of <!--$reservedStorageGb-->reservedStorageGb<!--/$reservedStorageGb--> GB between <!--$minTime-->minTime<!--/$minTime--> and <!--$maxTime-->maxTime<!--/$maxTime-->.

In this state, insert, update, delete, and index maintenance queries or any other requests that require system or user database space expansion will fail immediately due to the insufficient space.
<!--/issueDescription-->

## **Recommended Steps**

To enable normal operation of your instance, please increase the storage limit from:

* [Azure Portal](https://portal.azure.com/)
	1. Navigate to the Managed Instance *<!--$ServerName-->ServerName<!--/$ServerName-->*
	2. Select *"Pricing Tier"*
	3. Increase storage size
	4. Click *"Apply"*

* [Az PowerShell - Managed Instance update](https://docs.microsoft.com/powershell/module/Az.Sql/Set-AzSqlInstance)

	Example (with the current values):

	`Set-AzSqlInstance -ResourceGroupName <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> -Name <!--$ServerName-->ServerName<!--/$ServerName--> -VCore <!--$virtualCoreCount-->virtualCoreCount<!--/$virtualCoreCount--> -StorageSizeInGB <!--$reservedStorageGb-->reservedStorageGb<!--/$reservedStorageGb-->`

* [Azure CLI - Managed Instance update](https://docs.microsoft.com/cli/azure/sql/mi#az-sql-mi-update)

	Example (with the current values):

	`az sql mi update --subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> --resource-group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> --name <!--$ServerName-->ServerName<!--/$ServerName--> --capacity <!--$virtualCoreCount-->virtualCoreCount<!--/$virtualCoreCount--> --storage <!--$reservedStorageGb-->reservedStorageGb<!--/$reservedStorageGb-->`

## **Recommended Documents**

* [Managed Instance resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits)
* [Managed Instance service tiers](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-service-tiers)
