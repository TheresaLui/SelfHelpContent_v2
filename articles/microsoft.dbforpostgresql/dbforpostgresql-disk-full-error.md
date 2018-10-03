<properties
	pageTitle="Orcas Postgres Server marked Readonly"
	description="Orcas Postgres Server Not Writable As Server Storage Is Full"
	infoBubbleText="Found PostgreSQL server readonly. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="seanliang,pranabm"
	displayOrder="100"
	articleId="dbforpostgresql-disk-full-error"
	diagnosticScenario="OrcasPostgresServerNotWritable"
	selfHelpType="rca"
	supportTopicIds="32569395"
	resourceTags="windows, linux"
	productPesIds="16222" 
	cloudEnvironments="public"
/>
# Orcas Postgres Server marked readonly As Server Storage Is Full

<!--issueDescription-->
During our investigation we determined that the database server was marked as read only. All transactions that makes an attempt to write (Insert/Update/Delete) to the server is expected to fail.

While the service attempts to make the server read-only, all new write transaction requests are blocked and existing active transactions will continue to execute. When the server is set to read-only, all subsequent write operations and transaction commits fail. Read queries will continue to work uninterrupted. After you increase the provisioned storage, the server will be ready to accept write transactions again.

The server is marked read-only when the amount of free storage reaches less than 5 GB or 5% of provisioned storage, whichever is less. For example:

a) If you have provisioned 100 GB of storage, and the actual utilization goes over 95 GB, the server is marked read-only. 

b) Alternatively, if you have provisioned 5 GB of storage, the server is marked read-only when the free storage reaches less than 250 MB.


<!--/issueDescription-->

## **Recommended steps**
1. To fix this issue please increase the storage size using the portal as described in [Reaching storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers).

2. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement. 

## **Recommended documents**
[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)

[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL)