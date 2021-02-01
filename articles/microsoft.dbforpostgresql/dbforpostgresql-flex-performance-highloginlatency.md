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

* Monitor the resource consumption of your server. If you are maxing out IO, memory or compute resources, scale up the resource that you are limited on.
* If your client is hosted in an Azure VM, use accelerated networking for lowest connection latency
* Use connection pooling to avoid the overhead of setting up many short-lived connections

## **Recommended Documents**

* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
