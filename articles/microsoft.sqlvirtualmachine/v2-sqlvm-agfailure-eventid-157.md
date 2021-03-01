<properties
	pageTitle="Availability Group Failure, Failover, Sync issue"
	description="Availability Group Failure, Failover, Sync issue"
	infoBubbleText="Availability Group Failure, Failover, Sync issue"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,amamun,babarmav"	
	authors="ujpat,amamun,babarmav"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740064"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="9fcfe64d-4ddb-4297-b5cc-a2ce93f87d10"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **EventId 157 - Disk was surprised removed** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

This can happen if the 

- There is significant disk IO [throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics). Follow [Performance Guidelines](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices?WT.mc_id=Portal-Microsoft_Azure_Support) for SQL Server on Azure VM to avoid IO throttling. 
- Storage Spaces property AutomaticClusteringEnabled is set to True f**or an AG Environment**- **change it to false**. 
- Running [Cluster validation Report](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012) **with Storage option**
