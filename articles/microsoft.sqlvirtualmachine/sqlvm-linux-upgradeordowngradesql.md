<properties
	pageTitle="sql administration/upgrade or downgrade a SQL edition"
	description="sql administration/upgrade or downgrade a SQL edition"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="egranet"
	ms.author="egranet"
	displayOrder=""
	articleId="f67a7233-d146-4fab-b610-2353f8239715"
	selfHelpType="generic"
	supportTopicIds="32633525"
	resourceTags="windowsSQL"
	productPesIds="16342"
	cloudEnvironments="public,fairfax"
	ownershipId="AzureData_AzureSQLVM"
/>

# sql administration/upgrade or downgrade a SQL edition

## **Recommended Steps**

* Upgrading to a new SQL version or edition: Currently, there is no in-place upgrade for SQL Server running in an Azure VM. Create a new Azure virtual machine with the desired SQL Server version/edition, and then migrate your databases to the new server using [standard data migration techniques](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-migrate-sql/).
