<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	ms.author="jan-eng"
	displayOrder="100"
	articleId="dbformysql-asc-40613-16"
	diagnosticScenario="OrcasMySQLGatewayCannotStartProxyConneciton"
	selfHelpType="rca"
	supportTopicIds="32628367"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect MySQL database server

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for MySQL. The Azure database for MySQL service uses a gateway as the service endpoint to provide layered security, high availability, and elastic scaling of resources with minimal downtime. During our investigation we found that the gateway was failing to establish connections to your host database server preventing you from connecting to your server. We have restarted the gateway and subsequently observed that connections are succeeding as expected. The issue has been forwarded to the engineering team for further monitoring and determining a permanent fix.
<!--/issueDescription-->

## **Recommended Steps**

As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mysql/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
