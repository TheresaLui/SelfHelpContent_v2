<properties
	pageTitle="Orcas MariaDB Server planned failover"
	description="RCA - Server planned failover"
	infoBubbleText="Server planned failover detected. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformariadb-planned-failover"
	diagnosticScenario="OrcasMariaDBPlannedFailOver"
	selfHelpType="rca"
	resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Can't connect MariaDB database server

<!--issueDescription-->
During our investigation regarding connection issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we determined that the server was restarted at <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) causing connection attempts to fail. The server restarted because planned failover due to <!--$RCA-->RCA<!--/$RCA-->.
<!--/issueDescription-->

## **Recommended Steps**

1. Errors like the above are transient in nature and your database server will come back online automatically. Please try to reconnect to your server to see if the server is back online.
2. As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mariadb/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMariaDB)
