<properties
	pageTitle="Orcas MariaDB Server unplanned failover"
	description="RCA - Server unplanned failover"
	infoBubbleText="Server unplanned failover detected. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformariadb-unplanned-failover"
	diagnosticScenario="OrcasMariaDBUnplannedFailOver"
	selfHelpType="rca"
	resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# Can't connect MariaDB database server

<!--issueDescription-->
During our investigation regarding connection issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we determined that the server was restarted at <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) causing connection attempts to fail. The server restarted because unplanned failover due to <!--$RCA-->RCA<!--/$RCA-->.
<!--/issueDescription-->

## **Recommended Steps**

As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mariadb/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMariaDB)
