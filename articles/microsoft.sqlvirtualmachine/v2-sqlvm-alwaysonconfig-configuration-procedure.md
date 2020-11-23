<properties
	pageTitle="AlwaysOn Availability Groups - Configuration"
	description="AlwaysOn Availability Groups - Configuration"
	infoBubbleText="AlwaysOn Availability Groups - Configuration"
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
	articleId="9d7b751e-c1b9-4fac-aa84-21f3b4157d0e"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 


<!--issueDescription--> 

Most users can resolve issues concerning **configuring Availability Groups** by using the following steps.

<!--/issueDescription--> 
 

## **Recommended Steps** 

-  **Different ways to Configure Availability Groups in Azure VMsS** 

   There are different ways to set up Availability Groups, as shown in the following list. See **[an overview and comparison of these different setups](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-overview#deployment)**. 

	* [Configure Availability Group prerequisites](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-prerequisites-tutorial) and follow the steps for [Always on Configuration-Manually](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial) 

	* [Use PowerShell or Az CLI to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-az-commandline-configure?tabs=azure-cli) 

	* [Use Azure Quick Start templates to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-quickstart-template-configure) 

	* [Configure an Availability Group using Azure Portal-Preview](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-azure-portal-configure?tabs=azure-cli) 

* **Configuring Load Balancer with Listener** 

    * On Azure virtual machines, SQL Server availability group requires a [load balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer). To configure Listener, follow [these instructions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#configure-listener) 
    * If you have set up an Availability Group across different Azure Regions, you will need one [load balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-multiple-regions#create-remote-replica) in each region. 
  * You have to use same load balancer if you have multiple Availability Groups in the same region. You must [add the additional IPs to the existing load balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-listener-powershell-configure#Add-IP) for additional AGs. 

* **Configure Basic Availability Group on Standard Edition** 
 
   Always On [Basic Availability Groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/basic-availability-groups-always-on-availability-groups?view=sql-server-ver15) provide a high-availability solution for SQL Server 2016 and SQL Server 2017 Standard Edition. A Basic Availability Group supports a failover environment for a single database. With a Basic Availability Group, you have many other [additional limitations](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/basic-availability-groups-always-on-availability-groups?view=sql-server-ver15#limitations). For Basic AG, you can use [Database Mirroring Connection String](https://docs.microsoft.com/sql/database-engine/database-mirroring/connect-clients-to-a-database-mirroring-session-sql-server?view=sql-server-ver15#example-connection-string) instead of a load balancer. 

* **Things to Keep in Mind when Configuring Always On Availability Groups** 

   - Before deploying Always On AGs, review [Performance Guidelines for your VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices) 
   - The VMS where you set up an Availability Group should be a part of an [Availability Set](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets#create-an-availability-set) or an [Availability Zone](https://docs.microsoft.com/azure/availability-zones/az-overview). Each node will have its own local storage. There is no Shared Storage concept in an Always On Availability Group. 
  - If your Availability Group spans across Azure and on-premises environments (a hybrid environment), you will still need a load balancer. 
  - If you are using SQL 2019 CU8+ on Windows 2016, you can [use DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-distributed-network-name-dnn-listener-configure) instead of a load balancer 

## **Recommended Documents** 

* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15) 
* [Add a Replica to Always On](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/use-the-add-replica-to-availability-group-wizard-sql-server-management-studio?view=sql-server-ver15) 
* [Join a Secondary Replica to Always On AG](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/join-a-secondary-replica-to-an-availability-group-sql-server?view=sql-server-ver15) 
* [Enable TDE on a Database in AG](https://techcommunity.microsoft.com/t5/sql-server-support/how-to-enable-tde-encryption-on-a-database-in-an-availability/ba-p/318086) 
* [Configure Read Only Routing for Availability Group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-read-only-routing-for-an-availability-group-sql-server?view=sql-server-ver15) 

