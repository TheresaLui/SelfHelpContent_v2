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
There are various ways and Steps involved in configuring Availability Groups which are listed below.
<!--/issueDescription-->

## **Recommended Steps**

- **Configuring Availability Groups in Azure VMS**

     There are 4 ways you can configure Availability Groups on an Azure VM. **Please check the Pre-requisite**s listed for each in their respective articles before you configure them:
 
  * [Use Azure Quick-start templates to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-quickstart-template-configure)
  * [Use PowerShell or Az CLI to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-az-commandline-configure?tabs=azure-cli)
  * [Configure Availability Group Using Azure Portal-Preview](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-azure-portal-configure?tabs=azure-cli)
  * [Configure Availability Group Pre-requisites](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-prerequisites-tutorial) and follow the steps for [Always on Configuration-Manually](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial)

* **Configuring Load Balancer with Listener**
  
    * On Azure virtual machines, a SQL Server availability group requires a [Load Balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer). Once you configured the Load Balancer, you can then [Configure Listener](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#configure-listener)
    * If you have Setup Always on across different Azure Region then you will need an [Additional Load Balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-multiple-regions#create-remote-replica)

 
* **Configure Basic Availability Group on Standard Edition**

  Always On [Basic Availability Groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/basic-availability-groups-always-on-availability-groups?view=sql-server-ver15) provide a high availability solution for SQL Server 2016 and SQL Server 2017 Standard Edition. A basic availability group supports a failover environment for a single database.  With Basic Availability Group you have many other [Limitations listed here](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/basic-availability-groups-always-on-availability-groups?view=sql-server-ver15#limitations)
  


* **Things to Keep in Mind when Configuring Always On Availability Groups**

   - Review best [Performance Guidelines for your VMS](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices) before you plan to deploy Always On
   - The VMS where you need to setup Availability Group should be a part of [Availability Set](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets#create-an-availability-set) or [Availability Zone](https://docs.microsoft.com/azure/availability-zones/az-overview). Each node will have its own storage and there is no Shared Storage concept in Always on Availability Group

  - If you have your Primary Replica on On-Premise, you will still need a load balancer for your DR site on Azure for High Availability. Only 1 IP Address will be online for a Listener when you have created Always on Across multiple Regions. 

  - If you are using SQL 2019 CU8+ on Windows 2016, you can [use DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-distributed-network-name-dnn-listener-configure) instead of load balancer

  - Clustering of SSIS, SSRS and SSAS services is not recommended with Always On.


## **Recommended Documents**

* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15)
* [Add a Replica to Always On](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/use-the-add-replica-to-availability-group-wizard-sql-server-management-studio?view=sql-server-ver15)
* [Join a Secondary Replica to Always On AG](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/join-a-secondary-replica-to-an-availability-group-sql-server?view=sql-server-ver15)
* [Enable TDE on a Database in AG](https://techcommunity.microsoft.com/t5/sql-server-support/how-to-enable-tde-encryption-on-a-database-in-an-availability/ba-p/318086)
* [Configure Read Only Routing for Availability Group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-read-only-routing-for-an-availability-group-sql-server?view=sql-server-ver15)

