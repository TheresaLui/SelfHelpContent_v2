<properties
    pageTitle="Replicate data into Azure Database for MySQL Single Server"
    description="Replicate data into Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna,bahusse"
    displayOrder="350"
    selfHelpType="generic"
    supportTopicIds="32747581"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="acef0171-21da-493e-89e0-8202602a9b5b"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Replicate data into Azure Database for MySQL - Single Server

Data-in replication lets you synchronize data from a MySQL server running on-premises, in virtual machines, or database services hosted by other cloud providers into the Azure Database for MySQL Single Server. Data-in Replication is based on the binary log (`binlog`) file position-based replication native to MySQL.

## **Recommended Steps**

* Review [considerations and limitations](https://docs.microsoft.com/azure/mysql/concepts-data-in-replication#limitations-and-considerations) of data-in replication
* Review how to configure [data-in replication](https://docs.microsoft.com/azure/mysql/howto-data-in-replication)
* If the master server has SSL enabled, make sure the SSL CA certificate provided for the domain has been included in the `mysql.az_replication_change_master` stored procedure. See [these examples](https://docs.microsoft.com/azure/mysql/howto-data-in-replication#link-master-and-replica-servers-to-start-data-in-replication) and the `master_ssl_ca` parameter.
* Make sure that the master server's IP address has been added to the Azure Database for MySQL replica server's firewall rules. Update firewall rules using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli).
* Make sure that the machine hosting the master server allows both inbound and outbound traffic on port 3306
* Make sure that the the master server has **Public IP address** or the DNS is public accessible

**Troubleshooting replication lag?** 

Review [Common scenarios for high replication latency](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-replication-latency#common-scenarios-for-high-replication-latency). Pay special attention to `binlog_group_commit_sync_delay parameter`, which controls how many microseconds the binary log commit waits before synchronizing the binary log file.

**Do all your tables have primary keys?** 

Azure Database for MySQL uses **ROW**-based binary logging. If your table is missing a primary key, all rows in the table are scanned for DML operations. This causes increased replication lag. To ensure that the replica is able to keep up with changes on the source, we generally recommend adding a primary key on tables in the source server before creating the replica server or re-creating the replica server if you already have one.

## **Recommended Documents**

* [How to configure data-in replication](https://docs.microsoft.com/azure/mysql/howto-data-in-replication)
* [Data-in replication stored procedures](https://docs.microsoft.com/azure/mysql/reference-data-in-stored-procedures)
* [Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/)
