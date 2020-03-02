<properties
  pageTitle="performance/alwayson"
	description="performance/alwayson"
	infoBubbleText=""
	service="microsoft.compute"
	resource="virtualmachines"
	authors="vadeveka"
	ms.author="vadeveka"
	displayOrder=""
	articleId="sqlvirtualmachine-performance-alwayson"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32633490,32633489"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	ownershipId="AzureData_AzureSQLVM"
/>

# performance/alwayson

## **Recommended Steps**

While running SQL Server in Azure Virtual Machines, we recommend that you continue using the same database performance [tuning options](https://docs.microsoft.com/azure/sql-database/sql-database-performance-guidance) that are applicable to SQL Server in on-premises server environment. However, the performance of a relational database in a public cloud depends on many factors such as the size of a virtual machine, and the configuration of the data disks. Please follow the [performance guidelines for SQL in Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance).

## **Recommended Documents**

* [Monitor performance for AlwaysOn availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/monitor-performance-for-always-on-availability-groups)
* [Troubleshooting availability group performance](https://blogs.msdn.microsoft.com/psssql/2018/04/05/lesson-learned-from-an-availability-group-performance-case/)
* [Performance best practices for SQL VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance/)<br>
* [Storage configuration guidelines for SQL VM](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2018/09/25/storage-configuration-guidelines-for-sql-server-on-azure-vm/)
* [OS best practice configurations for SQL Server](https://blogs.msdn.microsoft.com/docast/2018/02/01/operating-system-best-practice-configurations-for-sql-server/)
