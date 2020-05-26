<properties
    pageTitle="Replicate data into Azure Database for MySQL"
    description="Replicate data into Azure Database for MySQL server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="380"
    selfHelpType="generic"
    supportTopicIds="32673560"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fa773e3d-6e0c-4357-8463-654b38c10025"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Replicate data into Azure Database for MySQL server

Data-in Replication allows you to synchronize data from a MySQL server running on-premises, in virtual machines, or database services hosted by other cloud providers into the Azure Database for MySQL service. Data-in Replication is based on the binary log (binlog) file position-based replication native to MySQL.

## **Recommended Steps**

* Review [considerations and limitations](https://docs.microsoft.com/azure/mysql/concepts-data-in-replication#limitations-and-considerations) of data-in replication
* Review how to configure [data-in replication](https://docs.microsoft.com/azure/mysql/howto-data-in-replication)
* If the master server has SSL enabled, ensure the SSL CA certificate provided for the domain has been included in the "mysql.az_replication_change_master" stored procedure. Refer to the following [examples](https://docs.microsoft.com/azure/mysql/howto-data-in-replication#link-master-and-replica-servers-to-start-data-in-replication) and the "master_ssl_ca" parameter.
* Ensure the master server's IP address has been added to the Azure Database for MySQL replica server's firewall rules. Update firewall rules using the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli).
* Ensure the machine hosting the master server allows both inbound and outbound traffic on port 3306
* Ensure the the master server has **Public IP address** or the DNS is public accessible

## **Recommended Documents**

* How to [configure data-in replication](https://docs.microsoft.com/azure/mysql/howto-data-in-replication)
* Refer to the [data-in replication stored procedures](https://docs.microsoft.com/azure/mysql/reference-data-in-stored-procedures)
* [Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/)
