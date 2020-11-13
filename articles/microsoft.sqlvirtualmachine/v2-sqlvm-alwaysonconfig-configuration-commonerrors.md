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

# We ran diagnostics on your resource and found the below steps which can help you. 

 ## **Common Errors encountered while Configuring Availability Groups**

<!--issueDescription--> 

Below are the common errors you may encounter while configuring Availability Group<br> 
**Error Code:** <!--$errorCode-->[errorCode]<!--/$errorCode-->

<!--/issueDescription--> 

 

## **Recommended Steps** 

 

 

 

 

* **Steps to Follow to Avoid any Errors when Configuring Availability Groups and Listener** 

 

  - If you cannot **Join the database to existing AG** then [Please review](https://techcommunity.microsoft.com/t5/SQL-Server-Support/Create-Availability-Group-Fails-With-Error-35250-Failed-to-join/ba-p/317987) 

 

  - Make sure **Port** 1433 (SQL Port), 5022(Endpoint Port) and 59999(Load balancer Probe Port) is not blocked at NSG or Windows Firewall on all replicas. Try to create Inbound/Outbound rules accordingly. 

  

   - Ensure that the **[NT AUTHORITY\SYSTEM]** account is [granted sufficient permissions](https://support.microsoft.com/help/2847723/cannot-create-a-high-availability-group-in-microsoft-sql-server-2012) on all replicas participating in Availability Group for Health Detection and for failing over your AG to another replica. 

 

  - If the **Create listener** fails with Message 19471 '**The WSFC cluster could not bring the Network Name resource online**' please review [this document](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online). 

 

 

 * **Unable to connect to AG listener from anywhere except the Primary replica node** 

 

      

 

 

      - Please ensure that a load balancer rule corresponding to the AG listener is [Configured](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#add-backend-pool-for-the-availability-group-listener). In Azure, a load balancer rule must be created for each AG listener. Please ensure that **Floating IP** (direct server return) is enabled for the load balancer.<br> 

 

 

     - Figure out the **Variables** using the below chart and ensure that you have [Run the PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#configure-listener) 

          

       

          * **Cluster Network Name:** In Failover Cluster Manager > Networks, right-click the network and select Properties. The correct value is under Name on the General tab. 

        * **SQL Server FCI/AG listener IP Address Resource Name:** In Failover Cluster Manager > Roles, under the SQL Server FCI role, under Server Name, right-click the IP address resource and select Properties. The correct value is under Name on the General tab.  

        * **ILBIP:** You can find it in Failover Cluster Manager on the same properties page where you located the &lt;SQL Server FCI/AG listener IP Address Resource Name&gt;. 

       * **nnnnn:** The probe port that you configured in the load balancer's health probe (such as 59999). Any unused TCP port is valid. 

 

 

         **NOTE**: After you run the PowerShell to configure the cluster parameters, restart the AG Role. 

 

 

 

 

## **Recommended Documents** 

* [Monitor and troubleshoot availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15) 

* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15) 

* [Use Cloud Witness For Quorum](https://docs.microsoft.com/windows-server/failover-clustering/deploy-cloud-witness) 

* [Add a Replica to Always On](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/use-the-add-replica-to-availability-group-wizard-sql-server-management-studio?view=sql-server-ver15) 

* [Join a Secondary Replica to Always On AG](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/join-a-secondary-replica-to-an-availability-group-sql-server?view=sql-server-ver15) 

