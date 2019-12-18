<properties
	pageTitle="Orcas MySQL Server Storage Over Threshold"
	description="Orcas MySQL Server Storage Over Threshold"
	infoBubbleText="Orcas MySQL Server Storage Over Threshold. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformysql-asc-storage-overthreshold"
	diagnosticScenario="OrcasMySQLStorageOverThresholdInsightV2TroubleShooter"
	selfHelpType="rca"
    resourceTags="servers, databases"
    cloudEnvironments="public"
/>

# Orcas MySQL Server storage usage is almost full

<!--issueDescription-->
During our investigation we determined that the database server storage usage is over <!--$StorageThreshold-->StorageThreshold<!--/$StorageThreshold-->% between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->.
<!--/issueDescription-->

Servers with less than 100 GB provisioned storage will be marked read-only if the free storage is less than 512MB or 5% of the provisioned storage size. Servers with more than 100 GB provisioned storage will be marked read only when the free storage is less than 5 GB. For example:

1. If you have provisioned 110 GB of storage, and the actual utilization goes over 105 GB, the server is marked read-only
2. Alternatively, if you have provisioned 5 GB of storage, the server is marked read-only when the free storage reaches less than 512 MB

The server will automatically be set to read/write again, when at least 5 GB of storage or 5% of the provisioned storage is free again.
<!--/issueDescription-->

## **Recommended Steps**

1. To fix this issue, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)
2. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql//)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
