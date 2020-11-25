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
	articleId="6cb481a4-81e6-46dd-8435-c44e754191968"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **Unable to connect to AG listener** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

- Ensure that the [load balancer](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#create-an-azure-load-balancer) is configured correctly.  
- Ensure that **[Floating IP (direct server return) is enabled](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial#set-the-load-balancing-rules)** for the load balancer.
- Figure out the variables by using the following list and ensure that you have **[run the PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-availability-group-tutorial#configure-listener)** 
  - **Cluster Network Name**: In Failover Cluster Manager > Networks, right-click the network and select **Properties**. The correct value is under Name on the General tab.
  - **SQL Server FCI/AG listener IP Address Resource Name**: In Failover Cluster Manager > Roles, under the SQL Server FCI role, under Server Name, right-click the IP address resource and select **Properties**. The correct value is under Name on the General tab.
  - **ILBIP**: You can find it in Failover Cluster Manager on the same properties page where you located the <SQL Server FCI/AG listener IP Address Resource Name>.
  - **nnnnn**: The probe port that you configured in the load balancer's health probe, such as 59999. Any unused TCP port is valid.

**Note:** After you run the PowerShell to configure the cluster parameters, restart the AG Role.
- Ensure that all the **ports required for the listener are open** in **[NSG](https://docs.microsoft.com/azure/virtual-machines/windows/nsg-quickstart-portal)** and in [Windows Firewall](https://docs.microsoft.com/windows/security/threat-protection/windows-firewall/create-an-inbound-port-rule) for all replicas. Specific examples: SQL instance port (1433), mirroring port (5022), load balancer probe port (59999).
- Ensure that SQL Server service is up and running on the Primary replica.
