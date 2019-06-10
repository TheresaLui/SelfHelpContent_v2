<properties
	pageTitle="Orcas MariaDB Server marked Readonly"
	description="Orcas MariaDB Server Not Writable As Server Storage Is Full"
	infoBubbleText="Found MariaDB server readonly. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="haz"
	displayOrder="100"
	articleId="dbformariadb-disk-full-error"
	diagnosticScenario="OrcasMariaDBServerNotWritable"
	selfHelpType="rca"
	supportTopicIds="32640117,32640118,32640120"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public"
/>

# Orcas MariaDB Server marked read-only because the server storage is full

<!--issueDescription-->
During our investigation we determined that the database server was marked as read-only. When a server is marked as read-only, all new transactions that try to write to the server (Insert/Update/Delete) are expected to fail. Read queries will continue to work uninterrupted.

The server is marked read-only when the amount of free storage goes below 5 GB or 5% of provisioned storage, whichever is less. For example:

1. If you have provisioned 100 GB of storage, and the actual utilization goes over 95 GB, the server is marked read-only.
2. Alternatively, if you have provisioned 5 GB of storage, the server is marked read-only when the free storage reaches less than 250 MB.

The server will automatically be set to read/write again, when at least 5 GB of storage or 5% of the provisioned storage is free again.
<!--/issueDescription-->

## **Recommended steps**

1. To fix this issue, please increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers).
2. You can increase the storage in the [Azure Portal](https://portal.azure.com) by clicking on the "Pricing Tier" and then scale up the storage as per your requirement.

## **Recommended documents**

[Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb//)

[MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMariaDB)
