<properties
    pageTitle="Troubleshooting login performance in Azure Database for MySQL"
    description="Troubleshooting login performance in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="savjani"
    ms.author="pariks"
    displayOrder="70"
    selfHelpType="generic"
    supportTopicIds="32640061"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6067320d-3cd3-4f10-874e-1ab970b383cd"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting login performance in Azure Database for MySQL

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