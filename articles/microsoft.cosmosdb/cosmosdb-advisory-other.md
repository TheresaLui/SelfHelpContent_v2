<properties
	pageTitle="Azure Cosmos DB - General Advisory"
	description="Azure Cosmos DB - General Advisory"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32741541"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-advisory-other"
	displayOrder="40"
	category="General Advisory"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB - General Advisory

Most users are able to resolve their General Advisory Questions using the steps below.

## **Recommended Steps**

### **Not able to create a new account or add a region (COVID-19)**

As companies operationalize to address new and unique challenges, we have mobilized our global response plan to help customers stay up and running during this critical time. We are actively monitoring performance and usage trends 24/7 to ensure we are optimizing our services for customers worldwide, while accommodating new demand. We are working closely with first responder organizations and critical government agencies to ensure we are prioritizing their unique needs and providing them our fullest support. We are also partnering with governments around the globe to ensure our local datacenters have on-site staffing and all functions are running properly.

As demand continues to grow, if we are faced with any capacity constraints in any region during this time, we have established clear criteria for the priority of new cloud capacity. Top priority will be going to first responders, health and emergency management services, critical government infrastructure organizational use, and ensuring remote workers stay up and running with the core functionality of Teams. We will also consider adjusting free offers, as necessary, to ensure support of existing customers.

As per the continuity plan, you may run into capacity constraints when performing the following operations:

1. Provision/Create a new Cosmos DB Account (including Free-Tier account)
2. Adding a region to an existing Cosmos DB Account
3. Create a new database/container in an existing Cosmos DB Account which does not have any container yet

However, you should be able to perform all operations against your existing Azure Cosmos DB resources in all regions without any restrictions.

If possible, please consider choosing any of the regions from **East US, East US 2, West US, West US 2, South Central US, North Europe, West Europe, Brazil South, Canada Central, France Central, Korea South or Korea Central** for new deployments which do not have any restrictions as of now.

For further information, please review our [commitment and service continuity](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity/).

If this is very critical for your business to have a new account or adding a region to an existing account, please continue creating a support ticket to explore other options.  

**Note**: If you are having issues other than the operations listed above, please continue with the below information to see if that helps resolve your issue.

### **Unable to register for Preview Features**

Issue: I want to preview some new features but I am not able to complete the registration in the portal.

- The account may be missing the required permission
- The subscription also would require Resource Provider "Microsoft.Features" to be registered

For additional information please see [Microsoft.Features](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftfeatures).

### **Data backup retention**

Azure Cosmos DB automatically takes a backup of your database every 4 hours and at any point of time, only the latest 2 backups are stored. However, if the container or database is deleted, Azure Cosmos DB retains the existing snapshots of a given container or database for 30 days.

<br>We do have the option to increase the backups retention duration to help you customize.  

There are some limits for the backups:

* Backups cannot be retained for more than 30 days
* The number of backups cannot be more than 25 at the same time
* The minimum backup interval is 1 hour  

## **Recommended Documents**

[How to model and partition in Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-model-partition-example)
<br>This article builds on several Azure Cosmos DB concepts like data modeling, partitioning, and provisioned throughput to demonstrate how to tackle a real-world data design exercise.  

[Cosmos DB Limits](https://docs.microsoft.com/azure/cosmos-db/concepts-limits)
<br>This article provides an overview of the default quotas offered to different resources in the Azure Cosmos DB.  

[Cosmos DB FAQs](https://docs.microsoft.com/azure/cosmos-db/faq)
<br>Frequently asked questions about different APIs in Azure Cosmos DB.  

[Azure Cosmos DB backup and restore process and policy](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore)
<br>This article describes how Azure Cosmos DB performs data backup.  

[Multi-region accounts](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account)
<br>This article describes how to manage various tasks on an Azure Cosmos account using the Azure portal, Azure PowerShell, Azure CLI, and Azure Resource Manager templates.  

[Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article describes the Key benefits of global distribution:
* Build global active-active apps
* Highly responsive apps
* Highly available apps
* Maintain business continuity during regional outages
* Scale read and write throughput globally
* Choose from several well-defined consistency models
