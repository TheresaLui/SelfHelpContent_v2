<properties
    pageTitle="Error while scaling a resource in Azure Database for MariaDB"
    description="Error while scaling a resource in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="170"
    selfHelpType="generic"
    supportTopicIds="32640119"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="50905891-e140-4f61-a758-41493777c12d"
    />

# Error while scaling a resource in Azure Database for MariaDB

In Azure Database for MariaDB, scaling can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * In case you want to migrate from Basic to General purpose/Memory Optimized and vice-versa, you can take a database dump of your Basic tier MariaDB database, recreate the server in General Purpose/Memory Optimized and then load the database dump and vice-versa.


* No new connections can be established when the system scales:

    * When you change the number of vCores or the pricing tier, a copy of the original server is created with the new compute allocation. After the new server is up and running, connections are switched over to the new server. During the moment when the system switches over to the new server, no new connections can be established, and all uncommitted transactions are rolled back. This window varies, but in most cases, is less than a minute.

* Cannot scale up the master server when a replica exists:

    * The replica must be scaled before master server

* Cannot scale down the replica of a master server:

    * The master server must scaled before replica server

## **Recommended Documents**

* [Azure Database for MariaDB Pricing Page](https://azure.microsoft.com/pricing/details/mariadb/)<br>
* [Read Replica in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-read-replicas#replica-configuration/)
