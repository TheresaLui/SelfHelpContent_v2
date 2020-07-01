<properties
	pageTitle="performance/SQL Server is slow"
	description="performance/SQL Server is slow"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	authors="yareyes, amamun"
	ms.author="yareyes, AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740098"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="7647ab12-e478-4fca-a2f0-c6df8cfe753b"
	ownershipId="AzureData_AzureSQLVM"
/>
# Performance/SQL Server is slow

## **Recommended Steps**

- For SQL Server on Azure VM, we **strongly recommend** that you follow the [Performance Guidelines for SQL Server on Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance).
- To understand **best practice violations and guest VM performance issues** you can [run Performance diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics) and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. See [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights).

To ensure a speedy resolution, please provide us the PerfInsights logs if you create a support case.

### **Other Things to Consider**
We recommend that you continue using the same database performance [tuning options](https://docs.microsoft.com/archive/msdn-magazine/2008/january/sql-server-uncover-hidden-data-to-optimize-application-performance) that are applicable to SQL Server in any SQL server environment: 
* Consider adding [missing indexes](https://gallery.technet.microsoft.com/Find-statements-for-13e8c2f4) which can help improve query performance
* Consider [updating statistics](https://docs.microsoft.com/sql/relational-databases/maintenance-plans/update-statistics-task-maintenance-plan?view=sql-server-ver15) if possible with Full Scan and for all tables of the database(s) of interest


## **Recommended Documents**

* [Performance best practices for SQL VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance/)<br>
* [Storage configuration guidelines for SQL VM](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2018/09/25/storage-configuration-guidelines-for-sql-server-on-azure-vm/)
* [OS best practice configurations for SQL Server](https://blogs.msdn.microsoft.com/docast/2018/02/01/operating-system-best-practice-configurations-for-sql-server/)
* [Azure VM Storage performance and throttling demystified](https://blogs.technet.microsoft.com/xiangwu/2017/05/14/azure-vm-storage-performance-and-throttling-demystify/)
* [Designing for high performance](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)
