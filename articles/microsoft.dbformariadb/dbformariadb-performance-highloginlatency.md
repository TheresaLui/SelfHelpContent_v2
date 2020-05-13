<properties
    pageTitle="Troubleshooting login performance in Azure Database for MariaDB"
    description="Troubleshooting login performance in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="70"
    selfHelpType="generic"
    supportTopicIds="32640126"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b71ef4af-4275-4188-8ec3-8d34d9bcc3fb"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Troubleshooting login performance in Azure Database for MariaDB

Slow login issues can have many different root causes. Work through the recommended steps to solve for the most common issues.

## **Recommended Steps**

* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.
* If your client is hosted in an Azure VM, turn on accelerated networking for lowest connection latency
* Use connection pooling on the client whenever possible to avoid overhead for establishing new connections

## **Recommended Documents**

* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)
