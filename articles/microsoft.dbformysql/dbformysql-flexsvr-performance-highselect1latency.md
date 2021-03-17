<properties
    pageTitle="Troubleshooting high latency when executing Select '1' in Azure Database for MySQL Flexible Server"
    description="Troubleshooting high latency when executing Select '1' in Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="savjani"
    ms.author="pariks"
    displayOrder="230"
    selfHelpType="generic"
    supportTopicIds="32747617"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b217332a-c05d-4cd8-a57c-7fc6b86b120d"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting high latency when executing Select '1' in Azure Database for MySQL Flexible Server

The time taken to execute 'Select 1' is a common way to measure the network latency between the client and the MySQL database. Most customers optimize the latency by working through the recommended steps.

## **Recommended Steps**

* Ensure your client and Azure Database for MySQL Flexible server are in the same Azure region
* If your client is hosted in an Azure VM or VMSS, turn on accelerated networking for lowest connection latency
* If you are connecting from the Azure Kubernetes Service, review the [Develop with Azure Kubernetes Service](https://docs.microsoft.com/azure/mysql/concepts-aks) documentation
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. Connection pooling is strongly recommended to avoid the overhead of establishing new connections
* For Java applications use [Hikari](https://github.com/brettwooldridge/HikariCP) for connection pooling
* For Php applications, use persistent connections and leverage [ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842) with builtin connection pooling
* Reduce the number of round trips between your application and the database if possible


## **Recommended Documents**

* [Azure Regions](https://azure.microsoft.com/global-infrastructure/regions/)<br>
* [Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli/)


