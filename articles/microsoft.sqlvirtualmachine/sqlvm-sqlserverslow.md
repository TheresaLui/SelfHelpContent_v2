<properties
	pageTitle="performance/sql server slow"
	description="performance/sql server slow"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	ms.author="yareyes"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32633522,32633520"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="f83877ee-08c5-4c00-bb48-67eb77055a2b"
	ownershipId="AzureData_AzureSQLVM"
/>

# performance/sql server slow

## **Recommended Steps**

While running SQL Server in Azure Virtual Machines, we recommend that you continue using the same database performance [tuning options](https://docs.microsoft.com/azure/sql-database/sql-database-performance-guidance) that are applicable to SQL Server in on-premises server environment. However, the performance of a relational database in a public cloud depends on many factors such as the size of a virtual machine, and the configuration of the data disks. 

- Please follow the [performance guidelines for SQL in Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
- Add any missing indexes which can help improve query performance
- **Did you know Performance diagnostics can help you analyze guest VM issues?** For Windows virtual machines, you can [run Performance diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics) and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. See [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights).

## **Recommended Documents**

* [Performance best practices for SQL VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance/)<br>
* [Storage configuration guidelines for SQL VM](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2018/09/25/storage-configuration-guidelines-for-sql-server-on-azure-vm/)
* [OS best practice configurations for SQL Server](https://blogs.msdn.microsoft.com/docast/2018/02/01/operating-system-best-practice-configurations-for-sql-server/)
* [Azure VM Storage performance and throttling demystified](https://blogs.technet.microsoft.com/xiangwu/2017/05/14/azure-vm-storage-performance-and-throttling-demystify/)
* [Designing for high performance](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)
