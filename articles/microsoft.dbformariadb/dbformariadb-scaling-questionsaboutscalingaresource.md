<properties
    pageTitle="Scaling Azure Database for MariaDB servers"
    description="Scaling Azure Database for MariaDB servers"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32640148"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="634e9e51-3804-4776-911d-d90d1cd5a6bc"
    />

# Scaling Azure Database for MariaDB servers

In Azure Database for MariaDB, scaling can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * In case you want to migrate from Basic to General purpose/Memory Optimized and vice-versa, you can take a database dump of your Basic tier MariaDB database, recreate the server in General Purpose/Memory Optimized and then load the database dump and vice-versa.

* Connections are dropped and no new connections can be established while vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MariaDB server once the scale operation is completed. Storage scaling does not cause a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

    * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

## **Recommended Documents**

* [Azure Database for MariaDB Pricing Page](https://azure.microsoft.com/pricing/details/mariadb/)<br>
* [Migrate to Azure Database for MariaDB using dump and restore](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore/)
* [Scaling resources in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers#scale-resources/)
