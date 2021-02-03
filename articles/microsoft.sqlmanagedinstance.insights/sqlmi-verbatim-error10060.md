<properties
	pageTitle="Error 10060 detected in detailed error message"
	description="Error 10060 detected in detailed error message"
	infoBubbleText="Error 10060 detected in detailed error message"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi_verbatim_10060"
	diagnosticScenario="SqlMIConnectivity"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI_Connectivity"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Based on the error message provided, we detected that the client cannot connect to the server. This usually indicates a client-side networking issue that you will need to pursue with your local network administrator.
<!--/issueDescription-->

## **Recommended Steps**

**Connecting via VPN (private endpoint)**

SQL Managed Instance is placed inside the Azure virtual network and a subnet that is dedicated to managed instances. This deployment provides you with a secure private IP address. You can connect to SQL Managed Instance via private endpoint if you are connecting from one of the following:
- Machine inside the same virtual network
- Machine in a peered virtual network
- Machine that is network-connected by VPN or Azure ExpressRoute

If you are trying to connect via private endpoint, review the following:
- Your machine has virtual network access to managed instance
- The host name is valid, format is <mi_name>.<dns_zone>.database.windows.net
- The port used for the connection is 1433 and you have firewalls and Network Security Groups (NSG) open to allow access on ports 1433
- If the [connection type](https://docs.microsoft.com/azure/azure-sql/managed-instance/connection-types-overview) is Redirect, and firewalls and Network Security Groups (NSG) are open to allow access on ports 11000-11999

Learn more about how to [connect your application to Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/connect-application-instance).

**Connecting via Public Endpoint**

If the machine does not have virtual network access to managed instance, you can use [public endpoint](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-configure) for data access to your managed instance from outside the virtual network. For example, this allows access from multi-tenant Azure services like Power BI, Azure App Service, or an on-premises network, via a public endpoint. 

If you are trying to connect via public endpoint, review the following:
- You have [Public Endpoint enabled](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-configure#enabling-public-endpoint-for-a-managed-instance-in-the-azure-portal)
- The [host name is valid](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-configure#obtaining-the-managed-instance-public-endpoint-connection-string), format is <mi_name>.public.<dns_zone>.database.windows.net,3342
- The port used for the connection is 3342, as mentioned earlier: [Inbound security rule was added in the NSG for port 3342](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-configure#allow-public-endpoint-traffic-on-the-network-security-group)

To learn more, see [how to configure public endpoint in Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-configure)
