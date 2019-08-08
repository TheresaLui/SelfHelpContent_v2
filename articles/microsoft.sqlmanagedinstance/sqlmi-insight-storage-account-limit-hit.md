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
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	articleId="sqlmanagedinstance-perf-storage-account-limit-hit"
/>

# Managed Instance - Storage account limit hit

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> had degraded performance between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> due to storage account limit being hit.
<!--/issueDescription-->

Every database file in SQL MI is placed on a separate Azure Premium disk (one file per disk). Azure Premium disks that are used in storage layer have fixed sizes: 128 GB, 256 GB, 512 GB, 1 TB, 2 TB, and 4 TB, and Managed Instance uses minimal disk size that is required to fit the database file with specified size. For example, database file with 200 GB will be placed on 256 GB disk, a database file with 800 GB will be placed on 1 TB disk. Every disk automatically grows if the database file size reaches the disk storage limits.

Every Managed Instance has up to 35 TB of total internal storage reserved for Azure Premium disks storage layer. If you create many files and the total size of the underlying disks reaches 35 TB, you will get internal storage limit error. This means that once you provision Managed Instance you have two storage limits:

1. Managed instance user-defined storage is the Managed Instance max storage size for your database files that you choose on portal and you pay for this amount of storage.
2. Internal physically allocated azure premium disk storage that cannot exceed 35 TB.

As a result, you cannot have more than 280 files on the General Purpose instance because 280 files placed on the smallest 128GB disks will reach 35TB limit.

You can reach this 35 TB limit even with the smaller number of files (less than 280). For example, a Managed Instance could have one database file with 2.2 TB that is placed on a 4 TB disk, and 248 files each 1 GB size that are placed on separate 128 GB disks. In this example, the total disk storage size is 1 x 4 TB + 248 x 128 GB = 35 TB. However, the total reserved space for database files on the instance is 1 x 2.2 TB + 248 x 1 GB = 2.4 TB. This illustrates that under certain circumstance, due to a very specific distribution of files, a Managed Instance might reach the 35 TB reserved for attached Azure Premium Disk when you might not expect it to.
