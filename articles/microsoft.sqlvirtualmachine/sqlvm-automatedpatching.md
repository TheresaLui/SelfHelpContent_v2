<properties
	pageTitle="sql administration/automated patching"
	description="sql administration/automated patching"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="yareyes"
	authors="yareyes"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32633492"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	articleId="90e771d6-e07b-4b7a-a550-5979fcf25d6b"
	ownershipId="AzureData_AzureSQLVM"
/>

# sql administration/automated patching

**Automated Patching** establishes a maintenance window for an Azure Virtual Machine running SQL Server. Automated Updates can only be installed during this maintenance window. For SQL Server, this restriction ensures that system updates and any associated restarts occur at the best possible time for the database.

Only Windows updates marked **Important** are installed. Other SQL Server updates, such as Cumulative Updates, must be installed manually. Automated Patching depends on the [SQL Server IaaS Agent Extension](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension). To find pre-requisites, see [Automated Patching for SQL Server in Azure Virtual Machines (Resource Manager)](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-automated-patching).

## **Recommended Documents**

* [Automated Patching for SQL Server in Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-automated-patching)<br>
