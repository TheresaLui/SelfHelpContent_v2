<properties
    pageTitle="Troubleshooting login performance in Azure Database for PostgreSQL"
    description="Troubleshooting login performance in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="70"
    selfHelpType="generic"
    supportTopicIds="32639986, 32781008"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="82efa5d3-1209-4364-b209-0c31ed1ca485"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting login performance

Slow login issues can have many different root causes. Work through the recommended steps to solve for the most common issues.

## **Recommended Steps**

* Monitor the resource consumption of your server. If you are maxing out IO, memory or compute resources, scale up the resource that you are limited on.
* If your client is hosted in an Azure VM, use accelerated networking for lowest connection latency
* Creating a new connection in Azure database for PostgreSQL - Single Server can take 100-300ms, there we recommend using [connection pooling](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/not-all-postgres-connection-pooling-is-equal/ba-p/825717) on the client whenever possible to avoid overhead of frequently establishing new connections. We recommend [pgBouncer](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/steps-to-install-and-setup-pgbouncer-connection-pooling-proxy/ba-p/730555).

## **Recommended Documents**

* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
