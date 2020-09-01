<properties
	pageTitle="Orcas PostgreSQL server marked read-only"
	description="Orcas PostgreSQL server not eritable because server storage is full"
	infoBubbleText="Found PostgreSQL server read-only. See details on the right"
	service="microsoft.dbforpostgresql"
	resource="dbforpostgresql"
	authors="seanliang"
	ms.author="zhlian"
	displayOrder="100"
	articleId="dbforpostgresql-disk-full-error"
	diagnosticScenario="OrcasPostgresServerNotWritable"
	selfHelpType="rca"
	supportTopicIds="32628458, 32628418"
	resourceTags="windows, linux"
	productPesIds="16222, 17067"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# PostgreSQL server marked read-only because server storage is full

<!--issueDescription-->
During our investigation we determined that the database server was marked as read-only. When a server is marked as read-only, all new transactions that try to write to the server (Insert/Update/Delete) are expected to fail. Read queries will continue to work uninterrupted.
<!--/issueDescription-->

Servers with less than 100 GB provisioned storage are marked read-only if the free storage is less than 512MB or 5% of the provisioned storage size. Servers with more than 100 GB provisioned storage are marked read only when the free storage is less than 5 GB. For example:

* If you have provisioned 110 GB of storage, and the actual utilization goes over 105 GB, the server is marked read-only
* Alternatively, if you have provisioned 5 GB of storage, the server is marked read-only when the free storage reaches less than 512 MB

The server will automatically be set to read/write again, when at least 5 GB of storage or 5% of the provisioned storage is free again.
<!--/issueDescription-->

## **Recommended Steps**

1. To fix this issue, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers)
2. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement

## **Recommended Documents**

* [Azure Database for PostgreSQL](https://azure.microsoft.com/services/postgresql/)
* [PostgreSQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforPostgreSQL)
