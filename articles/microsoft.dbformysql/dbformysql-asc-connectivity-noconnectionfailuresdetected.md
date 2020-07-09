<properties
	pageTitle="Orcas MySQL server no connection failures detected"
	description="RCA - Orcas MySQL server no connection failures detected"
	infoBubbleText="No connection failures detected."
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformysql-asc-connectivity-noconnectionfailuresdetected"
	diagnosticScenario="OrcasMySQLNoSystemErrorsInsightV2TroubleShooter"
	selfHelpType="rca"
	supportTopicIds="32640053, 32640051"
	resourceTags="servers, databases"
	cloudEnvironments="public, blackForest, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# No MySQL server connection failures detected

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName-->. Please note that we have checked our backend telemetry and noticed that there were no database side errors in the provided time range <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC).
<!--/issueDescription-->

## **Recommended Steps**

Please consider reviewing your application side for potential connectivity issues or errors, like:

* Application side firewall blocking outbound connections, please consider trying a public network to connect to the database to test connectivity
* High resource utilization on the application side
* DNS resolution issues
* Make sure the connection string is in the right format, see [this](https://docs.microsoft.com/azure/mysql/howto-connection-string) for more details
* Outdated/unsupported client driver, see [MySQL supported drivers](https://docs.microsoft.com/azure/mysql/concepts-compatibility)

## **Recommended Documents**

* [Azure Database for MySQL connection strings](https://docs.microsoft.com/azure/mysql/howto-connection-string)
* [Azure Database for MySQL supported client drivers](https://docs.microsoft.com/azure/mysql/concepts-compatibility)
* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)