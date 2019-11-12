<properties
	pageTitle="Server unplanned failover"
	description="RCA - Server unplanned failover"
	infoBubbleText="Server unplanned failover detected"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="zhlian"
	ms.author="zhlian"
	displayOrder="100"
	articleId="dbforpostgresql-asc-unplanned-failover"
	diagnosticScenario="OrcasPostgresUnplannedFailOver"
	selfHelpType="rca"
	supportTopicIds="32628416"
	resourceTags="windows, linux"
	productPesIds="16222"
	cloudEnvironments="public"
/>
# Can't connect PostgreSQL database server

<!--issueDescription-->
The server <!--$ServerName-->ServerName<!--/$ServerName--> was restarted at <!--$StartTime-->StartTime<!--/$StartTime-->. The server restarted because unplanned failover due to <!--$RCA-->RCA<!--/$RCA-->.
<!--/issueDescription-->

<<<<<<< HEAD
## **Recommended documents**

[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)

[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)

[Handling transient connectivity errors for Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/concepts-connectivity)
=======
## **Recommended Steps**

As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforPostgreSQL)
>>>>>>> origin/master
