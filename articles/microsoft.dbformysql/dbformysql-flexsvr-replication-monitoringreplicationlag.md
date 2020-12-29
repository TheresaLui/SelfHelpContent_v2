<properties
    pageTitle="Monitoring replication in Azure Database for MySQL - Flexible Server"
    description="Monitoring replication in Azure Database for MySQL - Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="330"
    selfHelpType="generic"
    supportTopicIds="32747626"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2bd68f3c-2187-4626-940b-4ecb678161bc"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Monitoring replication in Azure Database for MySQL - Flexible Server

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* The *Replication lag* metric doesn't show any data: The **Replication Lag** metric is only applicable to replica servers. For each replica, this metric reflects the time since the last transaction that was replayed on that replica. The source server does not show data for this metric.
* The *Replica Lag* metric is showing high replication lag: refer to [troubleshoot replication latency in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency).
* The *Replica lag* metric is increasing: Confirm if the configuration of the replica server matches the source. For example, if you have increased the source server vCores, ensure the replica server's vCores are equal or greater than the  .

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)
* [Troubleshoot replication latency in Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/troubleshooting-replication-latency-in-azure-database-for-mysql/ba-p/1752473)
* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)
* [Pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=mysql/)