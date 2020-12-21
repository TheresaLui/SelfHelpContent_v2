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
	articleId="18158c08-2a66-41bf-a746-654657e53c66"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **Unable to failover AG** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

- Ensure that the **[ NT AUTHORITY\SYSTEM account is granted required privilege](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012)** on all the replicas of the AG.
- Watch from the cluster manager while you do the failover. Do the IP address and network name come online? If not, resolve the IP or network name issues.
