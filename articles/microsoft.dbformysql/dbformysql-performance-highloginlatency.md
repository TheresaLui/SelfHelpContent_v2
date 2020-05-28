<properties
    pageTitle="Troubleshooting login performance in Azure Database for MySQL"
    description="Troubleshooting login performance in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
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

Slow login issues can have many different root causes. Work through the recommended steps to solve for the most common issues.

## **Recommended Steps**

* Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.
* If your client is hosted in an Azure VM, turn on accelerated networking for lowest connection latency
* Use connection pooling on the client whenever possible to avoid overhead for establishing new connections
* If you are connecting from the Azure Kubernetes Service, review the [Develop with Azure Kubernetes Service](https://docs.microsoft.com/azure/mysql/concepts-aks) documentation

## **Recommended Documents**

* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
