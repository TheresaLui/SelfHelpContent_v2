<properties
	pageTitle="Orcas MySQL Server unplanned failover"
	description="RCA - Server unplanned failover"
	infoBubbleText="Server unplanned failover detected. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformysql-unplanned-failover"
	diagnosticScenario="OrcasMySQLUnplannedFailOver"
	selfHelpType="rca"
	resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect MySQL database server

<!--issueDescription-->
During our investigation regarding connection issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName--> we determined that the server was restarted at <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) causing connection attempts to fail. The server restarted because unplanned failover due to <!--$RCA-->RCA<!--/$RCA-->.
<!--/issueDescription-->

## **Recommended Steps**

As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mysql/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
