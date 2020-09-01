<properties
	pageTitle="Connect to Server Failed Because of Firewall"
	description="RCA - Connect to Server Failed Because of Firewall RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	ms.author="zhlian"
	authors="seanzqliang"
	displayOrder="100"
	articleId="dbforpostgresql-asc-connectivity-firewallrules"
	diagnosticScenario="OrcasPostgresFirewall"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Failed connections to PostgreSQL server due to firewall restriction

<!--issueDescription-->
There are <!--$Count-->Count<!--/$Count--> failed connections to PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName--> between <!--$StartTime-->StartTime<!--/$StartTime-->(UTC) and <!--$EndTime-->EndTime<!--/$EndTime-->(UTC) because the originating IP addresses are not allowed to access this server.
<!--/issueDescription-->

## **Recommended Steps**

* You can either specify a single IP address or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/). Alternatively, you can use [virtual network rules](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet).
* The server's IP may appear to be public because you can ping or connect using telnet. However, connections to an Azure Database for PostgreSQL server are first routed through a publicly accessible Azure gateway. The actual server is protected by a firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture).

## **Recommended Documents**

* [Firewall rule concepts in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)
* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
* [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
