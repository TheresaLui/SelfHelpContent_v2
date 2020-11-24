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
	articleId="fe0e47de-a012-4e2a-81f8-9b1da60caadf"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 
Most users can resolve issues concerning **AG is offline or databases are in resolving state** by using the following steps.
<!--/issueDescription--> 
 
## **Recommended Steps** 

- Make sure that  **Windows cluster service is running**. 
- Make sure that **[cluster network thresholds are relaxed](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster)**
- If **[cluster service was started with force quorum](https://docs.microsoft.com/sql/sql-server/failover-clusters/windows/force-a-wsfc-cluster-to-start-without-a-quorum?view=sql-server-ver15)**,  you [must use following command](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/perform-a-forced-manual-failover-of-an-availability-group-sql-server?view=sql-server-ver15) in the correct replica to bring AG online:  
`ALTER AVAILABILITY GROUP AGName FORCE_FAILOVER_ALLOW_DATA_LOSS`
- Account **[NT AUTHORITY\SYSTEM has required privileges](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012)** 
