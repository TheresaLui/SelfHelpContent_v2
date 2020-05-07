<properties
	pageTitle="Orcas MariaDB server is running Out of Connections"
	description="RCA - Orcas MariaDB server is running Out of Connections"
	infoBubbleText="Server is running Out of Connections. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformariadb-asc-connectivity-outofconnections"
	diagnosticScenario="OrcasMariaDBOutofConnectionsInsightV2TroubleShooter"
	selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Can't connect MariaDB database server because of running out of connections

<!--issueDescription-->
During our investigation regarding connection issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we found that <!--$Count-->Count<!--/$Count--> connection attempts to fail due to connections to your database server have been running out between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC).
<!--/issueDescription-->

## **Recommended Steps**

* Try to reduce the number of concurrent connections by closing idle connections. We recommend using a [connection pooler](https://docs.microsoft.com/azure/mysql/concepts-connectivity#access-databases-by-using-connection-pooling-recommended) to manage connections.
* Ensure you have chosen a compute tier that can support the maximum number of connections required by the application

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums)
