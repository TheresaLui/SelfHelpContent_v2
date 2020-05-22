<properties
    pageTitle="Troubleshooting maximum connection limit in Azure Database for MariaDB"
    description="Troubleshooting maximum connection limit in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="60"
    selfHelpType="generic"
    supportTopicIds="32640153"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ceaae45b-62e8-4c63-b68f-8660e3bce04d"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Troubleshooting maximum connection limit in Azure Database for MariaDB

Each active connection consumes memory and therefore the maximum number of connections allowed depends upon the chosen pricing tier. Higher pricing tiers have more  memory and hence higher limits on maximum connections

## **Recommended Steps**

* Ensure you have chosen the appropriate pricing tier that can support the maximum number of connections required by the application
* Try to reduce the number of concurrent connections by closing idle connections or better by using connection pooling on the client

## **Recommended Documents**

* [MariaDB Max connections](https://docs.microsoft.com/azure/mariadb/concepts-limits)<br> 
* [Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/)
