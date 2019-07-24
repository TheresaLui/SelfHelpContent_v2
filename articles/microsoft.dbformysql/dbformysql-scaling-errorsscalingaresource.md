<properties
    pageTitle="Error while scaling a resource in Azure Database for MySQL"
    description="Error while scaling a resource in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="170"
    selfHelpType="resource"
    supportTopicIds="32640054"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="58f4750d-e3ae-4f4d-96c6-f0eb789ae5f7"
/>

# Error while scaling a resource in Azure Database for MySQL

In Azure Database for MySQL, scaling can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * Scaling only supported from General Purpose to Memory Optimized service tiers and vice-versa. Azure Database for MySQL does not allow any scaling to/from the Basic service tier.
    * In case you want to migrate from Basic to General purpose/Memory Optimized and vice-versa, you can take a database dump of your Basic tier MySQL database, recreate the server in General Purpose/Memory Optimized and then load the database dump and vice-versa.

* Can't change the backup storage type after a server is created:

    * You can independently change the vCores, the pricing tier (except to and from Basic), the amount of storage, and the backup retention period. You cannot change the backup storage type after a server is created.

* No new connections can be established when the system scales:

    * When you change the number of vCores or the pricing tier, a copy of the original server is created with the new compute allocation. After the new server is up and running, connections are switched over to the new server. During the moment when the system switches over to the new server, no new connections can be established, and all uncommitted transactions are rolled back. This window varies, but in most cases, is less than a minute.

* Cannot scale up the master server when a replica exists:

    * The replica must be scaled before master server

* Cannot scale down the replica of a master server:

    * The master server must scaled before replica server

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Read Replica in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#replica-configuration/)
