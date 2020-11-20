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
	articleId="a1b97491-6f53-42e0-9064-4a11cbeaa66c"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **There have been X misaligned log IOs** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 
- This can happen in hybrid environment like on-prem and Azure with [different disk sector sizes](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si). Please **[apply latest SQL Server patch](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)**  and use **[trace flag 1800 as startup parameter](https://support.microsoft.com/help/3009974/kb3009974-fix-slow-synchronization-when-disks-have-different-sector-si)**.