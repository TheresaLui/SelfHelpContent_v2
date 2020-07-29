<properties
    pageTitle="Replicate data into Azure Database for MariaDB"
    description="Replicate data into Azure Database for MariaDB server"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="410"
    selfHelpType="generic"
    supportTopicIds="32673562"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2b5fd4c3-692c-4b4b-a1c8-b553f15608d2"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Replicate data into Azure Database for MariaDB server

Data-in Replication allows you to synchronize data from a MariaDB server running on-premises, in virtual machines, or database services hosted by other cloud providers into the Azure Database for MariaDB service. Data-in Replication is based on the binary log (binlog) file position-based replication native to MariaDB.

## **Recommended Steps**

* Review [considerations and limitations](https://docs.microsoft.com/azure/mariadb/concepts-data-in-replication#limitations-and-considerations) of data-in replication
* Review how to configure [data-in replication](https://docs.microsoft.com/azure/mariadb/howto-data-in-replication)
* If the master server has SSL enabled, ensure the SSL CA certificate provided for the domain has been included in the "mariadb.az_replication_change_master" stored procedure. Refer to the following [examples](https://docs.microsoft.com/azure/mariadb/howto-data-in-replication#link-the-master-and-replica-servers-to-start-data-in-replication) and the "master_ssl_ca" parameter.
* Ensure the master server's IP address has been added to the Azure Database for MariaDB replica server's firewall rules. Update firewall rules using the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-portal) or [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-cli).
* Ensure the machine hosting the master server allows both inbound and outbound traffic on port 3306
* Ensure the the master server has **Public IP address** or the DNS is public accessible

## **Recommended Documents**

* How to [configure data-in replication](https://docs.microsoft.com/azure/mariadb/howto-data-in-replication)
* Refer to the [data-in replication stored procedures](https://docs.microsoft.com/azure/mariadb/reference-data-in-stored-procedures)
* [Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/)
