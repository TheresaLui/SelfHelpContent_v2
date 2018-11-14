<properties
	pageTitle="Server could not be found"
	description="RCA - Server could not be found"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	displayOrder="100"
	articleId="dbformysql-asc-18470-4"
	diagnosticScenario="OrcasMySQLServerNotFoundInBackend"
	selfHelpType="rca"
	supportTopicIds="32568715, 32568711"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public"
/>
# Can't connect MySQL database server because the server could not be found

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues with Azure Database for MySQL. The Azure database for MySQL service uses a gateway as the service endpoint to provide layered security, high availability, and elastic scaling of resources with minimal downtime. During our investigation we determined that connections to your database server are failing because the gateway cannot locate the server for the name specified as part of the user name.
<!--/issueDescription-->

## **Recommended steps**

To fix this issue, please ensure that the server name you specify as part of the user name is correct and matches the server name in the host name. You can refer to [this article](https://docs.microsoft.com/azure/mysql/howto-connection-string) for assistance with constructing a connection string for your Azure Database for MySQL sever.

## **Recommended documents**

[Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)

[MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforMySQL)