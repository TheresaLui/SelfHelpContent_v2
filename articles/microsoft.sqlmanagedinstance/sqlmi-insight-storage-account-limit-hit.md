<properties
	pageTitle="Managed Instance - Storage account limit hit"
	description="Managed Instance - Storage account limit hit"
	infoBubbleText="Managed Instance storage account limit of 35TB was hit. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="v-zlrade"
	authors="v-zlrade"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_StorageAccountLimitHit"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-perf-storage-account-limit-hit"
	ownershipId="AzureData_AzureSQLDB"
/>

# Managed Instance - Storage account limit hit

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> had issues adding and/or resizing database files between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> due to  35 TB storage account limit being hit.
<!--/issueDescription-->

Every database file in SQL MI <b>with General Purpose service tier </b>is placed on a separate Azure Premium disk (one file per disk). Azure Premium disks that are used in storage layer have fixed sizes: 128 GB, 512 GB, 1 TB, 2 TB, and 4 TB, and Managed Instance uses minimal disk size that is required to fit the database file with specified size. For example, database file with a size of 100 GB will be placed on 128 GB disk, a database file with 800 GB will be placed on 1 TB disk. Every Managed Instance with General Purpose service tier has up to 35 TB of total internal storage reserved for Azure Premium disks storage layer. If you create many files and the total size of the underlying disks reaches 35 TB, you will get internal storage limit error.

More detailed information about reaching storage account limit hit and how General Purposes instances use Azure disk storage for storing database files can be found at the [following link](<https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Reaching-Azure-disk-storage-limit-on-General-Purpose-Azure-SQL/ba-p/386234>).