<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	displayOrder="100"
	articleId="dbformysql-asc-40613-16"
	diagnosticScenario="OrcasMySQLGatewayCannotStartProxyConneciton"
	selfHelpType="rca"
	supportTopicIds="32568704, 32568715, 32568711"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public"
/>
# Can't connect MySQL database server

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for MySQL. The Azure database for MySQL service uses a gateway as the service endpoint to provide layered security, high availability, and elastic scaling of resources with minimal downtime. During our investigation we found that the gateway was failing to establish connections to your host database server preventing you from connecting to your server. We have restarted the gateway and subsequently observed connections succeeding as expected. The issue has been forward to the engineering team for further monitoring and to determine a permanent fix.
<!--/issueDescription-->

## **Recommended steps**

Because the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement re-try logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mysql/concepts-high-availability) for more details.

## **Recommended documents**

[Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
[MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforMySQL)