<properties
	pageTitle="IP not configured in firewall"
	description="RCA - Client IP not configured in firewall"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	ms.author="jan-eng"
	displayOrder="100"
	articleId="dbformysql-asc-18456-102"
	diagnosticScenario="OrcasMySQLIpNotInFirewall"
	selfHelpType="rca"
	supportTopicIds="32628367"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Can't connect MySQL database server because IP address is not configured in firewall

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for MySQL. During our investigation we determined that connections to your database server are failing because the client IP address is not configured as allowed IP address in the firewall of the server.
<!--/issueDescription-->

## **Recommended Steps**

To fix this issue please ensure your client IP address is configured in the firewall of the server. You can refer to [this article](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) for assistance with configuring your firewall for your Azure Database for MySQL server.

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
