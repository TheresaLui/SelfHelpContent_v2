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
	articleId="43dfaae4-ab56-43c6-b9bc-4799619b356f"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **Why didn't AG fail over?** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

Make sure that:
- **[Conditions for Automatic Failover](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/failover-and-failover-modes-always-on-availability-groups?view=sql-server-ver15#RequiredConditions)** are met. This means **every secondary database on the failover target is synchronized**
- The account **[NT AUTHORITY\SYSTEM has required privileges](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012)** 
- [Maximum Failures in the Specified Period" value is not exhausted](https://support.microsoft.com/help/2833707/kb2833707-troubleshooting-automatic-failover-problems-in-sql-server-20). 
