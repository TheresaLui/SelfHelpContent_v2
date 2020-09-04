<properties
    pageTitle="Troubleshooting login performance in Azure Database for MySQL Flexible Server"
    description="Troubleshooting login performance in Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="savjani"
    ms.author="pariks"
    displayOrder="240"
    selfHelpType="generic"
    supportTopicIds="32747618"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e0317652-cee5-4d49-a325-17c6120ee5e7"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting login performance in Azure Database for MySQL Flexible Server
Slow login issues can have many different root causes. Work through the recommended steps below to solve for the most common issues.

## **Recommended Steps**

* Try scaling up your compute size to next higher vCores and Memory and see if it helps improve login issues. If you max out either CPU or Memory resources, it can cause slow login issues.
* If your client is hosted in an Azure VM or VMSS, turn on accelerated networking for lowest connection latency.
* If you are connecting from the Azure Kubernetes Service, review the [Develop with Azure Kubernetes Service](https://docs.microsoft.com/azure/mysql/concepts-aks) documentation.
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. Connection pooling is strongly recommended to avoid the overhead of establishing new connections.
* For Java applications use [Hikari](https://github.com/brettwooldridge/HikariCP) for connection pooling.
* For Php applications, use persistent connections and leverage [ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842) with builtin connection pooling. 
* Reduce the number of round trips between your application and the database if possible.

## **Recommended Documents**

* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
* [Azure Regions](https://azure.microsoft.com/global-infrastructure/regions/)<br>
* [Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli/)

