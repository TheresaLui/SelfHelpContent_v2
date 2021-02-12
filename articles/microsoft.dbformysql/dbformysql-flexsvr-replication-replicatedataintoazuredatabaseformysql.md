<properties
    pageTitle="Replicate data into Azure Database for MySQL - Flexible Server"
    description="Replicate data into Azure Database for MySQL - Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="340"
    selfHelpType="generic"
    supportTopicIds="32747633"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b0675b19-a5ca-48f6-a7e8-53a17167bc2b"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Replicate data into Azure Database for MySQL - Flexible Server

Data-in Replication allows you to synchronize data from a MySQL server running on-premises, in virtual machines, or database services hosted by other cloud providers into the Azure Database for MySQL - Flexible Server. Data-in Replication is based on the binary log (binlog) file position-based replication native to MySQL.

## **Recommended Steps**

* Ensure the SSL CA certificate provided for the domain has been included in the "mysql.az_replication_change_master" stored procedure.
* Ensure the machine hosting the master server allows both inbound and outbound traffic on port 3306
* Ensure the the master server has **Public IP address** or the DNS is public accessible

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)<br>
* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=mysql/)