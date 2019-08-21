<properties
    pageTitle="Scaling Azure Database for MySQL servers"
    description="Scaling Azure Database for MySQL servers"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32640086"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="d980b014-1500-4f79-a025-03717b4576da"
/>

# Scaling Azure Database for MySQL servers

In Azure Database for MySQL, scaling can only be done between General Purpose and Memory Optimized service tiers. Scaling to/from the Basic service tier is not supported.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Not able to scale from Basic to General Purpose/Memory Optimized service tiers and vice-versa:

    * In case you want to migrate from Basic to General purpose/Memory Optimized and vice-versa, you can take a database dump of your Basic tier MySQL database, recreate the server in General Purpose/Memory Optimized and then load the database dump and vice-versa.

* Connections are dropped and no new connections can be established while vCores are scaled:

    * vCore scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MySQL server once the scale operation is completed. Storage scaling does not cause a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

    * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Migrate to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)
* [Scaling resources in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#scale-resources/)
