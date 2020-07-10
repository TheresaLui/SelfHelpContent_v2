<properties
    pageTitle="High latency on Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="High select 1 or login latency on Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource="serverGroups"
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-performance-highlatency.md"
    selfHelpType="resource"
    supportTopicIds="32639985, 32639986"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshoot high latency 

Most customers optimize latency by working through the recommended steps.

## **Recommended Steps**

* Ensure your client and Hyperscale (Citus) server group are in the same Azure region
* If your client is hosted in an Azure VM or Azure Kubernetes Service, use accelerated networking for lowest connection latency
* Ensure you are measuring latency on an existing connection. Creating a new connection can take 100+ milliseconds. Connection pooling is recommended to avoid the overhead of establishing new connections.
* Reduce the number of round trips between your application and the database
* Monitor the resource consumption of your server group. If you are maxing out IO, memory or compute resources, scale up the resource that you are limited on or increase the number of worker nodes.


## **Recommended Documents**

* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
* [Scaling Hyperscale (Citus)](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-scaling)
