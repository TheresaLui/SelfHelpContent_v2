<properties
	pageTitle="Orcas PostgreSQL server marked read-only"
	description="Orcas PostgreSQL server not eritable because server storage is full"
	infoBubbleText="Found PostgreSQL server read-only. See details on the right"
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

# PostgreSQL server marked read-only because server storage is full

<!--issueDescription-->
During our investigation we determined that the database server was marked as read-only. When a server is marked as read-only, all new transactions that make an attempt to write to the server (Insert/Update/Delete) are expected to fail. Read queries will continue to work uninterrupted.

The server is marked read-only when the amount of free storage goes below 5 GB or 5% of provisioned storage, whichever is less. For example:

1. If you have provisioned 100 GB of storage, and the actual utilization goes over 95 GB, the server is marked read-only.
2. Alternatively, if you have provisioned 5 GB of storage, the server is marked read-only when the free storage reaches less than 250 MB.

The server will automatically be set to read/write again, when at least 5 GB of storage or 5% of the provisioned storage are free again.
<!--/issueDescription-->

## **Recommended steps**

1. To fix this issue, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/postgrsql/concepts-pricing-tiers).
2. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.

## **Recommended documents**

[Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)

[PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL)