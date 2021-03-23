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
	articleId="958d4026-9350-4af2-a8c9-79bf0e31296e"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **EventId 1196** Network name resource failed registration of associated DNS name by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

* **Event 1196**: Network name resource failed registration of associated DNS name

     * Check the NIC settings for each of your cluster nodes to make sure there are no external DNS records present

     * Ensure the A record for your cluster exists on your internal DNS servers. If not, create a new A Record manual in DNS Server for the Cluster Access Control object and check the Allow any authenticated users to update DNS Records with the same owner name.
    
     * Take the Resource "Cluster Name" with IP Resource offline and fix it.