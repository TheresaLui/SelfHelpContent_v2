<properties
    pageTitle="Troubleshooting high latency when executing Select '1' in Azure Database for MySQL Single Server"
    description="Troubleshooting high latency when executing Select '1' in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="savjani"
    ms.author="pariks"
    displayOrder="220"
    selfHelpType="generic"
    supportTopicIds="32747564"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f05b7720-82a1-4428-863f-9b2d44945dff"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting high latency with 'Select 1' in Azure Database for MySQL Single Server

The time taken to execute 'Select 1' is a common way to measure the network latency between the client and the MySQL database. Most customers optimize the latency by working through the recommended steps.

## **Recommended Steps**

* Ensure your client and Azure Database for MySQL Single server are in the same Azure region.
* If your client is hosted in an Azure VM or VMSS, turn on accelerated networking for lowest connection latency.
* If you are connecting from the Azure Kubernetes Service, review the [Develop with Azure Kubernetes Service](https://docs.microsoft.com/azure/mysql/concepts-aks) documentation.
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. Connection pooling is strongly recommended to avoid the overhead of establishing new connections.
* For Java applications use [Hikari](https://github.com/brettwooldridge/HikariCP) for connection pooling.
* For Php applications, use persistent connections and leverage [ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842) with builtin connection pooling. 
* Reduce the number of round trips between your application and the database if possible


## **Recommended Documents**

* [Azure Regions](https://azure.microsoft.com/global-infrastructure/regions/)<br>
* [Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli/)
