<properties
	pageTitle="AlwaysOn Availability Groups - Setup Listener and Load Balancer"
	description="AlwaysOn Availability Groups - Setup Listener and Load Balancer"
	infoBubbleText="AlwaysOn Availability Groups - Setup Listener and Load Balancer"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740063,32740109"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="1d6f8725-f391-4668-9a5b-7d352b7806e7"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you.

<!--issueDescription-->
Below Steps can help you setup your Listener and Load Balancer for Availability Groups
<!--/issueDescription-->

## **Recommended Steps**

- **Configuring Load Balancer using Azure Portal**

   * On Azure virtual machines, a SQL Server availability group requires a [Load Balancer to be configured](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer).

  * If you have Setup Always on across different Azure Region then you will need an [Additional Load Balancer for the other region](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-multiple-regions#create-remote-replica)

   * Make sure Floating IP is enabled when you configure the Load Balancing Rule.

* **Configuring Listener for Availability Groups**
  
   * Once you configured the Load Balancer, you can then [Configure Listener](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#configure-listener)

  * **Listener May not show up** in SSMS if you pre-stage it. Add Listener dependency to AG Resource for it to show up in SSMS.

  * **Do not forget** to run the [PowerShell Script in this document](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-load-balancer-portal-configure) or else you wont be able to connect to the listener from any other machines except the Primary Replica. Once you run the PowerShell take the Listener Resource Offline and Bring it up again.

   * If the **Create listener fails** with Message 19471 'The WSFC cluster could not bring the Network Name resource online' please review [this document](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online).

* **Things to Keep in Mind when Configuring Listener or Load Balancer**

  * Availability group listeners can [share the same TCP port](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-listener-overview?view=sql-server-ver15#SelectListenerPort) within the same service process. So it is possible to use 1433  for different listeners

   * Configuring Load Balancer with Probe Port 80 is not recommended.

   * To avoid issues with Listener Connectivity, Make sure **Ports** 1433 (SQL Instance Port), 5022 (Mirroring Endpoint), 59999 (Probe Port)
  are not blocked at NSG or Windows Firewall. Make sure SQL instance is not using [Dynamic Ports](https://docs.microsoft.com/sql/tools/configuration-manager/tcp-ip-properties-ip-addresses-tab?view=sql-server-ver15#dynamic-ports)

  

## **Recommended Documents**

* [Create Standard SKU Load Balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-load-balancer-portal-configure)
* [Configure load balancer for AG VNN listener](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-vnn-azure-load-balancer-configure)
