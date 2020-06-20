<properties
    pageTitle="Cosmos DB connectors"
    description="Troubleshoot Azure Cosmos DB connectors"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32741539"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-connectors-other"
    displayOrder="121"
    category="Tools and Connectors"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Cosmos DB connectors
Most users are able to resolve their Connectors issue using the steps below.

## **Recommended Steps**  

### **Issues with Data explorer access for Cosmos DB**  

Please check your firewall rules.  If you have recently updated your firewall, the rule may be take up to 24 hours to be applied.  

### **Problem activating autoscale feature in Cosmos DB**  

Autoscale automatically scales the RU/s of your database or container between the max RU/s you set, and 0.1 * max RU/s.

* You can enable autoscale on existing databases and containers through the Azure portal. 
* To create new databases and containers with autoscale, use the Azure portal, Azure Resource Manager template, or latest versions of the Azure Cosmos DB .NET SDK V3.9+ or Java SDK V4+.
* Support in Azure CLI, PowerShell, and other SDKs is planned, but not yet available.



## **Recommended Documents**
[Supported Cosmos DB connectors](https://docs.microsoft.com/azure/cosmos-db/)
<br>Azure Cosmos DB documentation list of support.
