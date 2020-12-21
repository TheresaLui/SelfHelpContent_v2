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
	articleId="cb208005-6101-4f33-bdb2-2ad5f74e5f67"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **Unable to login after failover** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

- Ensure that you are using the AG Listener name or the [DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-distributed-network-name-dnn-listener-configure) to connect 
- [Listener is setup with a load balancer correctly](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer). 
- Appropriate logins are available in the new primary. Use Method 2 in [this article](https://support.microsoft.com//help/918992/how-to-transfer-logins-and-passwords-between-instances-of-sql-server) to transfer logins from previous primary to the new primary
