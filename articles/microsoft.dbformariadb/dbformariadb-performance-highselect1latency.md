<properties
    pageTitle="Troubleshooting high latency when executing Select 1 in Azure Database for MariaDB"
    description="Troubleshooting high latency when executing Select 1 in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="80"
    selfHelpType="generic"
    supportTopicIds="32640125"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="803dfa11-bd6e-479b-9554-8a7e934ea898"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Troubleshooting high latency with 'Select 1' in Azure Database for MariaDB

The time taken to execute 'Select 1' is a common way to measure the network latency between the client and the MariaDB database. Most customers optimize the latency by working through the recommended steps.

## **Recommended Steps**

* Ensure your client and MariaDB Database are in the same Azure region
* If your client is hosted in an Azure VM, turn on accelerated networking for lowest connection latency
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. Connection pooling is strongly recommended to avoid the overhead of establishing new connections.
* Reduce the number of round trips between your application and the database if possible
* We strongly recommend that you use a database connection pool or a long connection to Azure Database for MariaDB.

## **Recommended Documents**

* [Azure Regions](https://azure.microsoft.com/global-infrastructure/regions/)<br>
* [Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli/)
