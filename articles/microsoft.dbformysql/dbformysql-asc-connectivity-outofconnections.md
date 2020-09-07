<properties
	pageTitle="Orcas MySQL server is running Out of Connections"
	description="RCA - Orcas MySQL server is running Out of Connections"
	infoBubbleText="Server is running Out of Connections. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformysql-asc-connectivity-outofconnections"
	diagnosticScenario="OrcasMySQLOutofConnectionsInsightV2TroubleShooter"
	selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect MySQL database server because of running out of connections

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our investigation we found that <!--$Count-->Count<!--/$Count--> connection attempts to fail due to connections to your database server have been running out between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->.
<!--/issueDescription-->

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections. We recommend using a [connection pooler](https://docs.microsoft.com/azure/mysql/concepts-connectivity#access-databases-by-using-connection-pooling-recommended) to manage connections.
* Ensure you have chosen a compute tier that can support the maximum number of connections required by the application

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
