<properties
	pageTitle="AlwaysOn Availability Groups - Unable to connect using Listener"
	description="AlwaysOn Availability Groups - Unable to connect using Listener"
	infoBubbleText="AlwaysOn Availability Groups - Unable to connect using Listener"
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
	articleId="7acae9d0-64ac-41d2-9d8a-181212c60482"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 


<!--issueDescription--> 

Most users can resolve issues about **Unable to connect to the Listener** by using the following information. 


<!--/issueDescription--> 

 

## **Recommended Steps** 

1. On Azure virtual machines, a SQL Server Availability Group requires a Load Balancer to be configured correctly. Otherwise, Listener connectivity may fail. Check the [Load balancer Configuration](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer). Make sure **Floating IP** is enabled when you configure the Load Balancing Rule. 

2. Using the following chart, figure out the **Variables** and ensure that you have [run the PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#configure-listener): 
   - **Cluster Network Name:** In Failover Cluster Manager > Networks, right-click the network and select **Properties**. The correct value is under Name on the General tab. 
   - **SQL Server FCI/AG listener IP Address Resource Name:** In Failover Cluster Manager > Roles, under the SQL Server FCI role, under Server Name, right-click the IP address resource and select **Properties**. The correct value is under Name on the General tab.    
   - **ILBIP:** You can find it in Failover Cluster Manager on the same properties page where you located the &lt;SQL Server FCI/AG listener IP Address Resource Name&gt;. 
   - **nnnnn:** The probe port that you configured in the load balancer's health probe (such as 59999). Any unused TCP port is valid. 

    **Note**: After you run the PowerShell to configure the cluster parameters, restart the AG Role. 

**To avoid issues with Listener Connectivity:** 

1. Make sure SQL Instance Port (example **1433**), Mirroring Endpoint (example **5022**), Probe Port (example **59999**) are open. You can [Telnet](https://docs.microsoft.com/windows-server/administration/windows-commands/telnet) to the Port or use [Test-NetConnection](https://docs.microsoft.com/powershell/module/nettcpip/test-netconnection?view=win10-ps#example-3--test-tcp-connectivity-and-display-detailed-results) to check that connections are not blocked at **NSG or Windows Firewall**.  

2. Make sure SQL instance is running on **[Static Port](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-a-server-to-listen-on-a-specific-tcp-port?view=sql-server-ver15)**. 
**Note:** If you have configured listener on any port other than 1433, you must use the port number in the Client connection string (example ListenerName,Port) 

3. Make sure your instance is enabled for **TCP/IP Communication** and has the [Listen All](https://docs.microsoft.com/sql/tools/configuration-manager/tcp-ip-properties-ip-addresses-tab?view=sql-server-ver15#options) property set. Make sure browser service is running.  

4. If you are connecting outside from a different network or on premises, check with your network admin to make sure that your **company firewall** is not blocking these connections. 

5. If you are not able to connect to Listener, try to connect using SSMS with various combinations such as **(Listener name, port)** or **(Listener IP, port)** to make sure you are not having DNS name resolution issues. Check on DNS Server that the record for the Listener still exists and is pointing to the correct IP Address. 

6. You may see issues connecting to Listener if your **AG failed over**, or due to **[Lease Timeout](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-lease-healthcheck-timeout?view=sql-server-ver15#updating-cluster-and-always-on-timeout-values)**, or if you are having issues with [SQL Performance](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices) or [disk or VM throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows). Check the SQL error log to find out more. 

7. If Create Listener fails with **error message 19471**, "The WSFC cluster could not bring the Network Name resource online," review [this document](https://docs.microsoft.com/archive/blogs/alwaysonpro/create-listener-fails-with-message-the-wsfc-cluster-could-not-bring-the-network-name-resource-online). 

 ## **Recommended Documents** 

* [Configure Load Balancer and Listener Correctly](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer) 
* [Configure load balancer for AG VNN listener](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-vnn-azure-load-balancer-configure) 
