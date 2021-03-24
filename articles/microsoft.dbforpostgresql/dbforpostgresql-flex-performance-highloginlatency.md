<properties
    pageTitle="Troubleshooting login performance in Azure Database for PostgreSQL"
    description="Troubleshooting login performance in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="70"
    selfHelpType="generic"
    supportTopicIds="32781007"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-performance-highloginlatency"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting login performance

Slow login issues have many different root causes. Work through the following recommended steps to resolve the most common issues.

## **Recommended Steps**

* Try scaling up your compute size to next higher vCores and Memory and see if it helps improve login issues. If you max out either CPU or Memory resources, it can slow down logins.
* If your client is hosted in an Azure VM or VMSS, use accelerated networking for lowest connection latency
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. We recommend using [connection pooling](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/not-all-postgres-connection-pooling-is-equal/ba-p/825717) on the client whenever possible to avoid overhead of frequently establishing new connections. We recommend [pgBouncer](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/steps-to-install-and-setup-pgbouncer-connection-pooling-proxy/ba-p/730555).
* Reduce the number of round trips between your application and the database, if possible

## **Recommended Documents**

* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
