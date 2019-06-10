<properties
	pageTitle="IP not configured in firewall"
	description="RCA - Client IP not configured in firewall"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="janeng"
	displayOrder="100"
	articleId="dbformariadb-asc-18456-102"
	diagnosticScenario="OrcasMariaDBIpNotInFirewall"
	selfHelpType="rca"
	supportTopicIds="32640117,32640118,32640120"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public"
/>

# Can't connect MariaDB database server because IP address is not configured in firewall

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for MariaDB. During our investigation we determined that connections to your database server are failing because the client IP address is not configured as allowed IP address in the firewall of the server.
<!--/issueDescription-->

## **Recommended steps**

To fix this issue please ensure your client IP address is configured in the firewall of the server. You can refer to [this article](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-using-portal) for assistance with configuring your firewall for your Azure Database for MariaDB server.

## **Recommended documents**

[Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)

[MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforMariaDB)
