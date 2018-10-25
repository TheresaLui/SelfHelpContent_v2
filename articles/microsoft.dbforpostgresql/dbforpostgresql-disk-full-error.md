<properties
	pageTitle="Orcas PostgreSQL server marked readonly"
	description="Orcas PostgreSQL server not eritable because server storage is full"
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

# PostgreSQL server marked readonly because server storage is full

<!--issueDescription-->
During our investigation we determined that the database server was marked as readonly because the server storage is full. When a server is marked readonly all transactions that attempt to write (Insert/Update/Delete) to the server are expected to fail.
<!--/issueDescription-->

While the service attempts to make the server readonly, all new write transaction requests are blocked and existing active transactions will continue to execute. When the server is set to read-only, all subsequent write operations and transaction commits fail. Read queries will continue to work uninterrupted. After you increase the provisioned storage, the server will be ready to accept write transactions again.

The server is marked read-only when the amount of free storage reaches less than 5 GB or 5% of provisioned storage, whichever is less. For example:

1. If you have provisioned 100 GB of storage, and the actual utilization goes over 95 GB, the server is marked read-only.

2. Alternatively, if you have provisioned 5 GB of storage, the server is marked read-only when the free storage reaches less than 250 MB.

## **Recommended steps**

1. To fix this issue please increase the storage size using the portal as described in [Reaching storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers).

2. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.

## **Recommended documents**

[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL)