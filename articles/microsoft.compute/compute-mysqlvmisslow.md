<properties
	pageTitle="My SQL Server VM is slow"
	description="My SQL Server VM is slow"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="michco"
	displayOrder="25"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="WindowsSQL"
	productPesIds="14749"
	cloudEnvironments="public"
/>
    
# My SQL Server VM is slow

## **Recommended steps**
Try following steps to diagnose and mitigate SQL VM performance issues.

1. Use Premium Storage for production workloads and enable read caching (set Host caching option to ReadOnly)<br>
[Premium Storage documentation](https://azure.microsoft.com/documentation/articles/storage-premium-storage/)
2. Review performance best practices<br>
[Performance best practices for SQL Server in Azure Virtual Machines](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-performance/)
3. Troubleshoot generic SQL Server workload performance issues:<br>
[SQL Server Performance: Approach and Tools](https://docs.com/ajith-krishnan/8919/sql-server-performance-troubleshooting-approach)

## **Recommended documents**
[Provision a SQL Server Virtual Machine in the Azure Portal](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-portal-sql-server-provision/)<br>
[Migrating to Azure Premium Storage](https://azure.microsoft.com/documentation/articles/storage-migration-to-premium-storage/)