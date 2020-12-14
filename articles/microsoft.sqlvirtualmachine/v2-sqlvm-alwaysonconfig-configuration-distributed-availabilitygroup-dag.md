<properties
	pageTitle="AlwaysOn Availability Groups - Configure Distributed Availability Group (DAG)"
	description="AlwaysOn Availability Groups - Configure Distributed Availability Group (DAG)"
	infoBubbleText="AlwaysOn Availability Groups - Configure Distributed Availability Group (DAG)"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740063"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="4c1b664d-78fc-4816-bd21-e2e2b86366ae"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
 

<!--issueDescription--> 

Most users can resolve issues with **configuring Distributed Availability Groups** by using the following steps.


<!--/issueDescription--> 


## **Recommended Steps** 

- **Configuring Distributed Availability Groups in Azure VMS** 

   - To create a distributed availability group, you must create two availability groups, each with its own Listener and load balancer. You then combine these availability groups into a [Distributed Availability Group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-distributed-availability-groups?view=sql-server-ver15). More information is available [Here](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/distributed-availability-groups?view=sql-server-ver15) 
  - Create [a load balancer for each Listener.](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer) 

* **Things to Keep in Mind when Configuring Always on Distributed Availability Groups** 

  * The Distributed Availability Group is supported in SQL 2016 or later. 
  * In a Distributed AG Setup, WSFC clusters that host the individual availability groups can have different [major versions of Windows Server](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/distributed-availability-groups?view=sql-server-ver15#windows-server-versions-and-distributed-availability-groups). The major versions of SQL Server must be the same. For upgrade scenarios, you can use higher version for the target environment. 
 

## **Recommended Documents** 
 
* [Monitor distributed availability group health](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/distributed-availability-groups?view=sql-server-ver15#monitor-distributed-availability-group-health) 
* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15) 
* [SQL Server version and edition requirements for distributed availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/distributed-availability-groups?view=sql-server-ver15#sql-server-version-and-edition-requirements-for-distributed-availability-groups) 
