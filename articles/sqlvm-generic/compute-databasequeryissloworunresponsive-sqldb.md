<properties
	pageTitle="performance/database query is slow or unresponsive"
	description="performance/database query is slow or unresponsive"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32511137"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public"
/>

# performance/database query is slow or unresponsive

## **Recommended steps**
Try following steps to diagnose and mitigate SQL VM performance issues

1. Use Premium Storage for production workloads and enable read caching (set Host caching option to ReadOnly)<br>
[Premium Storage documentation](https://azure.microsoft.com/documentation/articles/storage-premium-storage/)
2. Review performance best practices<br>
[Performance best practices for SQL Server in Azure Virtual Machines](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-performance/)
3. Troubleshoot generic SQL Server workload performance issues:<br>
[SQL Server Performance: Approach and Tools](https://docs.com/ajith-krishnan/8919/sql-server-performance-troubleshooting-approach)
4. Note: SQL Server VMs created in the Portal with the Azure Resource Manager model implement best performance practices

## **Recommended documents**
[Performance best practices for SQL Server in Azure Virtual Machines](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-performance/)<br>
[Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/documentation/articles/storage-premium-storage/)<br>
[SQL Server Performance: Approach and Tools](https://docs.com/ajith-krishnan/8919/sql-server-performance-troubleshooting-approach)<br>
