<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783932"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Administration and Security/Synapse Workspace - Private Link"
    description = "Administration and Security/Synapse Workspace - Private Link"
    articleId = "synapse-cs-administrationandsecurity-synapseworkspaceprivatelink.md"
    ms.author = "saltug"
/>

# Administration and Security/Synapse Workspace - Private Link

## **Recommended Steps**

Private Link allows you to connect to various PaaS services in Azure via a private endpoint. For a list to PaaS services that support Private Link functionality, go to the [Private Link Documentation](https://docs.microsoft.com/azure/private-link/) page. A private endpoint is a private IP address within a specific VNet and Subnet. You can [setup a private link](https://docs.microsoft.com/azure/sql-database/sql-database-private-endpoint-overview?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json#how-to-set-up-private-link-for-azure-sql-database) for your SQL pool. Connections to private endpoint only support Proxy as the connection policy.

## **Recommended Documents**

* [Test connectivity to SQL Database from an Azure VM in same Virtual Network (VNet)](https://docs.microsoft.com/azure/sql-database/sql-database-private-endpoint-overview?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json#test-connectivity-to-sql-database-from-an-azure-vm-in-same-virtual-network-vnet)

* [On-premises connectivity over private peering](https://docs.microsoft.com/azure/sql-database/sql-database-private-endpoint-overview?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json#on-premises-connectivity-over-private-peering)

* [Connecting from an Azure Synapse Analytics Dedicated SQL pool to Azure Storage using Polybase](https://docs.microsoft.com/azure/sql-database/sql-database-private-endpoint-overview?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json#connecting-from-an-azure-sql-data-warehouse-to-azure-storage-using-polybase)

 