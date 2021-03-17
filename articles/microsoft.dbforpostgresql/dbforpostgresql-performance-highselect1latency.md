<properties
    pageTitle="High latency with Select 1"
    description="High latency with Select 1"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="80"
    selfHelpType="generic"
    supportTopicIds="32639985, 32781006"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="292fcc3a-3194-41db-9b6a-81cc343089fd"
    	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting high latency with 'Select 1'

Measuring the time it takes to run a `SELECT 1` query is a common way to measure the network latency between the client and the PostgreSQL database. Most customers optimize the latency by working through the following recommended steps.

## **Recommended Steps**

* Ensure your client and PostgreSQL Database are in the same Azure region
* If your client is hosted in an Azure VM, turn on accelerated networking for lowest connection latency
* If you are connecting from the Azure Kubernetes Service, review the [Develop with Azure Kubernetes Service](https://docs.microsoft.com/azure/postgresql/concepts-aks) documentation
* Ensure that you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. Connection pooling is strongly recommended to avoid the overhead of establishing new connections.
* Reduce the number of round trips between your application and the database if possible by batching multiple requests.
* We strongly recommend that you use a database connection pool or a long connection to Azure Database for PostgreSQL.

## **Recommended Documents**

* [Azure Regions](https://azure.microsoft.com/global-infrastructure/regions/)<br>
* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
