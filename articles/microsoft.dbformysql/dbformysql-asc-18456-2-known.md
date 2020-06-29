<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	ms.author="jan-eng"
	displayOrder="100"
	articleId="dbformysql-asc-18456-2-known"
	diagnosticScenario="OrcasMySQLBackendErrorKnownReasons"
	selfHelpType="rca"
	supportTopicIds="32628367"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect to MySQL database server

<!--issueDescription-->
During our investigation regarding connection issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName--> we determined that the server was restarted between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC), causing <!--$Count-->Count<!--/$Count--> connection attempts to fail. The server restarted because <!--$FailureCause-->FailureCause<!--/$FailureCause-->.
<!--/issueDescription-->

## **Recommended Steps**

1. Errors like the above are transient in nature and your database server will come back online automatically. Please try to reconnect to your server to see if the server is back online.
2. As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mysql/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
