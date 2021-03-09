<properties
    pageTitle="High latency with Select 1"
    description="High latency with Select 1"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="80"
    selfHelpType="generic"
    supportTopicIds="32781005"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-performance-highselect1latency"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting high latency with `Select 1`

The time taken to execute a `SELECT 1` query is a common way to measure the network latency between the client and the PostgreSQL database. Most customers can optimize the latency by working through the following recommended steps.

## **Recommended Steps**

* Ensure that your client and PostgreSQL Database are in the same Azure region
* If your client is hosted in an Azure VM, turn on accelerated networking for lowest connection latency
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. We strongly recommend connection pooling to avoid the overhead of establishing new connections.
* Reduce the number of round trips between your application and the database, if possible
* We strongly recommend that you use a database connection pool or a long connection to Azure Database for PostgreSQL.

## **Recommended Documents**

* [Azure Regions](https://azure.microsoft.com/global-infrastructure/regions/)<br>
* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
