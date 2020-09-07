<properties
    pageTitle="Limits in Azure Cosmos DB" 
    description="Limits in Azure Cosmos DB"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32636797"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-limits-quotas"
    displayOrder="200"
    category="Limits and quotas"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Limits in Azure Cosmos DB

The below recommended document provides an overview of the limits in the Azure Cosmos DB service. Most users are able to resolve their Limits case using the steps below.

## **Recommended Steps**

### **Not able to create a new account or add a region (COVID-19)**
As companies operationalize to address new and unique challenges, we have mobilized our global response plan to help customers stay up and running during this critical time. We are actively monitoring performance and usage trends 24/7 to ensure we are optimizing our services for customers worldwide, while accommodating new demand. We are working closely with first responder organizations and critical government agencies to ensure we are prioritizing their unique needs and providing them our fullest support. We are also partnering with governments around the globe to ensure our local datacenters have on-site staffing and all functions are running properly.

As demand continues to grow, if we are faced with any capacity constraints in any region during this time, we have established clear criteria for the priority of new cloud capacity. Top priority will be going to first responders, health and emergency management services, critical government infrastructure organizational use, and ensuring remote workers stay up and running with the core functionality of Teams. We will also consider adjusting free offers, as necessary, to ensure support of existing customers.

As per the continuity plan, you may run into capacity constraints when performing the following operations:

1. Provision/Create a new Cosmos DB Account(including Free-Tier account).
2. Adding a region to an existing Cosmos DB Account
3. Create a new database/container in an existing Cosmos DB Account which does not have any container yet.

However, you should be able to perform all operations against your existing Azure Cosmos DB resources in all regions without any restrictions.

If possible, please consider choosing any other region for new deployments which do not have any restrictions as of now.

For further information, please review our [commitment and service continuity](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity/).

If this is very critical for your business to have a new account or adding a region to an existing account, please continue creating a support ticket to explore other options.  

**Note** : If you are having issues other than the operations listed above, please continue with the below information to see if that helps resolve your issue.

Look for the specific limit or quota threshold and the appropriate way to raise the limit if needed. 

### **Document size cannot exceed 2 MB**  
Cosmos DB has a per document size limit of 2MB [Azure Cosmos DB Per-item limits.](https://docs.microsoft.com/azure/cosmos-db/concepts-limits#per-item-limits)  
**Solution:** If your requirements need to exceed this, it is recommended to split the document into multiple sub-documents and create a new field to link them together.  When retrieving, you would use a query to retrieve all documents that are linked together.  

## **Recommended Documents**

[Limits in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/concepts-limits)
<br>This article provides an overview of the default quotas offered to different resources in the Azure Cosmos DB.  

[How to enable autoscale on a database or container](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-autoscale-throughput?tabs=api-async)
<br> Autoscale automatically scales the RU/s of your database or container between the max RU/s you set, and 0.1 * max RU/s. 

You can enable autoscale on existing resources through the Azure portal. To create new autoscale resources, use an Azure Resource Manager template or the latest versions of the Azure Cosmos DB .NET SDK V3.9+ and Java SDK V4+. See this article for samples. 


[Request Unit Factors](https://docs.microsoft.com/azure/cosmos-db/request-units#request-unit-considerations)
<br>When estimating the number of RUs per second to provision, use this article to consider factors that impact RUs.  

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>With Azure Cosmos DB, you pay for the throughput you provision and the storage you consume on an hourly basis. Throughput must be provisioned to ensure that sufficient system resources are available for your Azure Cosmos database at all times. You need enough resources to meet or exceed the Azure Cosmos DB SLAs.  

