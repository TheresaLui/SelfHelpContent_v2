<properties
	pageTitle="AlwaysOn Availability Groups - Configuration - Common Errors"
	description="AlwaysOn Availability Groups - Configuration - Common Errors"
	infoBubbleText="AlwaysOn Availability Groups - Configuration - Common Errors"
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
	articleId="d68de188-b871-4571-8af2-7bb4c8cbe8ed"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue 

<!--issueDescription-->
Below are the common errors you may encounter while configuring Availability Group
<!--/issueDescription-->

## **Recommended Steps**


* **Steps to Follow to Avoid any Errors when Configuring Availability Groups and Listener**

  - If you cannot **Join the database to existing AG** then [Please review](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Create-Availability-Group-Fails-With-Error-35250-Failed-to-join/ba-p/317987)

  - Make sure Port 1433 (SQL Port), 5022(Endpoint Port) and 59999(Load balancer Probe Port) is not blocked at NSG or Windows Firewall on all replicas. Try to create Inbound/Outbound rules accordingly.
 
   - Ensure that the *[NT AUTHORITY\SYSTEM]* account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all replicas participating in Availability Group for Health Detection and for failing over your AG to another replica.

  - **Unable to Setup Listener**

    If the create listener fails with Message 19471 'The WSFC cluster could not bring the Network Name resource online' please review [this document](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online).

 * **Unable to connect to AG listener from anywhere except the Primary replica node**

     


     * **Is the load balancer correctly configured?**

       Please ensure that a load balancer rule corresponding to the AG listener is [Correctly Configured](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#add-backend-pool-for-the-availability-group-listener). In Azure, a load balancer rule must be created for each AG listener. Please ensure that Floating IP (direct server return) is enabled for the load balancer.<br>

    * **Have you ensured that the correct configuration changes have been made at WSFC level for the Load balancer and AG listener?**

       Please ensure that you have [Run the PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#configure-listener) with correct variables as below:

         ```
          $ClusterNetworkName = "<MyClusterNetworkName>" # the cluster network name (Use Get-ClusterNetwork on Windows Server 2012 
          of higher to find the name)
          $IPResourceName = "<IPResourceName>" # the IP Address resource name
          $ListenerILBIP = "<n.n.n.n>" # the IP Address of the Internal Load Balancer (ILB). This is the static IP address for the 
          load balancer you configured in the Azure portal.
          [int]$ListenerProbePort = <nnnnn>

          Import-Module FailoverClusters
          Get-ClusterResource $IPResourceName | Set-ClusterParameter -Multiple 
          @{"Address"="$ListenerILBIP";"ProbePort"=$ListenerProbePort;"SubnetMask"="255.255.255.255";
          "Network"="$ClusterNetworkName";"EnableDhcp"=0}
         ```
       **NOTE**: After you run the PowerShell to configure the cluster parameters, you must take the AG resource offline and online to ensure modifications take effect. You need to run the PowerShell on one node (VM) of the cluster only.


## **Recommended Documents**
* [Monitor and troubleshoot availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15)
* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15)
* [Use Cloud Witness For Quorum](https://docs.microsoft.com/windows-server/failover-clustering/deploy-cloud-witness)
* [Add a Replica to Always On](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/use-the-add-replica-to-availability-group-wizard-sql-server-management-studio?view=sql-server-ver15)
* [Join a Secondary Replica to Always On AG](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/join-a-secondary-replica-to-an-availability-group-sql-server?view=sql-server-ver15)


