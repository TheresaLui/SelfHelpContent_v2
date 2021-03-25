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

* Try scaling up your compute size to next higher vCores and Memory and see if it helps improve login issues. If you max out either CPU or Memory resources, it can slow down logins.
* If your client is hosted in an Azure VM or VMSS, use accelerated networking for lowest connection latency
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. We recommend using [connection pooling](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/not-all-postgres-connection-pooling-is-equal/ba-p/825717) on the client whenever possible to avoid overhead of frequently establishing new connections. We recommend [pgBouncer](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/steps-to-install-and-setup-pgbouncer-connection-pooling-proxy/ba-p/730555).
* Reduce the number of round trips between your application and the database if possible

## **Recommended Documents**

* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
