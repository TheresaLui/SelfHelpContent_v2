<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	displayOrder="100"
	articleId="dbformysql-asc-18456-2-known"
	diagnosticScenario="OrcasMySQLBackendErrorKnownReasons"
	selfHelpType="rca"
	supportTopicIds="32568704, 32568709"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public"
/>
# Can't connect to MySQL database server

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we determined that the server was restarted between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->, causing <!--$Count-->Count<!--/$Count--> connection attempts to fail. The server restarted because <!--$FailureCause-->FailureCause<!--/$FailureCause-->.
<!--/issueDescription-->

## **Recommended steps**

1. Errors like the above are transient in nature and your database server will come back online automatically. If you have not yet, please try to re-connect to your server.
2. Because the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement re-try logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mysql/concepts-high-availability) for more details.

## **Recommended documents**

[Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
[MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforMySQL)