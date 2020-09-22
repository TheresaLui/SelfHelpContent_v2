<properties
	pageTitle="Connect to Server Failed Because of Firewall"
	description="RCA - Connect to Server Failed Because of Firewall"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	ms.author="conwan"
	authors="congwang"
	displayOrder="100"
	articleId="dbformariadb-asc-connectivity-firewallrules"
	diagnosticScenario="OrcasMariaDBFirewall"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Failed connections to MariaDB server due to firewall restriction

<!--issueDescription-->
During our investigation we found that your server <!--$ServerName-->ServerName<!--/$ServerName--> has connectivity issues between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC) because the originating IP addresses are not allowed to access this server.
<!--/issueDescription-->

## **Recommended Steps**

* You can either specify a single IP address or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-portal), the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-cli), and our [REST API](https://docs.microsoft.com/rest/api/mariadb/). Alternatively, you can use [virtual network rules](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-vnet).
* The server's IP may appear to be public because you can ping or connect using telnet. However, connections to an Azure Database for MariaDB server are first routed through a publicly accessible Azure gateway. The actual server is protected by a firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mariadb/concepts-connectivity-architecture).

## **Recommended Documents**

* [Firewall rule concepts in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules)
* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)
* [Tutorial: Creating and connecting to Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal)
* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforMariaDB)
