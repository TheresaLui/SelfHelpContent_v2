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
	articleId="6557e79c-8ced-4a4e-8018-5d90b37263f7"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **AG db log file is growing or unable to shrink** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

- Review  [this article](https://support.microsoft.com/help/2922898/error-9002-the-transaction-log-for-database-full-due-to-availability) to understand/manage the AG database log file.
- Review [factors that can delay log truncation](https://docs.microsoft.com/sql/relational-databases/logs/the-transaction-log-sql-server?view=sql-server-ver15#FactorsThatDelayTruncation)
