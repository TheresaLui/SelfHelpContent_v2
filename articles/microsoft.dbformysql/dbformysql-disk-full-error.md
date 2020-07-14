<properties
	pageTitle="Orcas MySQL Server marked Readonly"
	description="Orcas MySQL Server Not Writable As Server Storage Is Full"
	infoBubbleText="Found MySQL server readonly. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="seanliang"
	ms.author="zhlian"
	displayOrder="100"
	articleId="dbformysql-disk-full-error"
	diagnosticScenario="OrcasMySQLServerNotWritable"
	selfHelpType="rca"
	supportTopicIds="32628367, 32628369"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Orcas MySQL Server marked read-only because the server storage is full

<!--issueDescription-->
During our investigation we determined that the database server was marked as read-only. When a server is marked as read-only, all new transactions that try to write to the server (Insert/Update/Delete) are expected to fail. Read queries will continue to work uninterrupted.
<!--/issueDescription-->

Servers with less than 100 GB provisioned storage are marked read-only if the free storage is less than 512MB or 5% of the provisioned storage size. Servers with more than 100 GB provisioned storage are marked read only when the free storage is less than 5 GB. For example:

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
