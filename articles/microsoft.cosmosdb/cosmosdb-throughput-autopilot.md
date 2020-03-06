<properties
	pageTitle="Autopilot"
	description="Troubleshoot Azure Cosmos DB throughput Autopilot issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32692540"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-throughput-autopilot"
	displayOrder="247"
	category="Core (SQL)"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Throughput Autopilot 
Most users are able to resolve their Throughput Autopilot issue using the steps below.

## **Recommended Steps**  

### Cannot find option to enable Autopilot?  
Autopilot has been registered for all users. Autopilot can only be enabled while creating new databases and containers from the Azure Portal.
- Support for CLI and SDK is not yet available
- Support to enable autopilot mode on existing containers and databases is not yet available

### I am trying to create the tables programmatically using ARM templates and cannot find the context for autopilot setting
- Support for CLI and SDK is not yet available

### Can I apply the Free Tier discount to autopilot databases and containers?
**Answer:** Yes. With autopilot, you are billed for the highest RUs the database or container scales to in the hour. When the free tier discount is applied, 400 RUs will be subtracted from that value. See our documentation for examples and details.  

### **FAQ**
**Is Autopilot supported on shared throughput databases?**
<br>Yes, autopilot is supported on provisioned collections as well as shared throughput database collections. Customer needs to choose the autopilot option at the time of database creation when using shared throughput.  
 
**Does autopilot feature applies to all the collections based on the cosmos account?**
<br>Autopilot is an offer you can use at the collection-level and does not apply to all the collections of your account. Once the preview is activated on your account, you can create collections with either the standard offer or with the autopilot one.  
 
**Is there a CLI / SDK support for creating containers / database with autopilot mode?**
<br>In the public preview currently the only supported way to create autopilot containers is via portal. SDK and CLI support will be added soon.  
 
**Portal only shows 4 max throughput values, how can I specify a different max throughput value?**
<br>In the public preview max throughput can be selected from a predefined list of values. In future we will allow letting user specify any arbitrary max throughput value and the autopilot feature will ensure that the container can scale between 0.1max to max.  
 
**What is the storage limit associated with a given max RUs?**
<br>Storage limit for a specified max RUs is calculated using this function (0.01 * Max RUs). If the container storage goes beyond the 0.01 * Max RUs, the maximum RUs is scaled up to the higher value from the list of 4 predefined limits.  
 
**Note**: Maximum throughput limit  - **Maximum storage limit**  
* 4000 RU/s - **50 GB**
* 20,000 RU/s - **200 GB**
* 100,000 RU/s - **1 TB**
* 500,000 RU/s  - **5 TB**  

**Is autopilot supported on all APIs?**
<br>Yes autopilot is supported on all the APIs: SQL , Mongo, Cassandra, Gremlin, Tables  
 
**Can autopilot be disabled on a container / database?**
<br>Yes we allow customer to move the autopilot container to a manually provisioned containers. But migrating back to autopilot is not allowed.  
 
**How much delay does autopilot have in reacting to a spike in traffic or traffic coming down?**
<br>Autopilot is instantaneous in providing capacity within the RU range of 0.1 * max and max. Both the scale up and scale down are instantaneous. Billing is done at a hourly granularity where the max RUs in that billing windows is considered.
 
**Is autopilot supported with multi-master accounts?**
<br>Yes 
 
**What happens if the incoming load reaches the max RUs?**
<br>Requests which exceed the max RUs will be throttled. Max RUs are calculated based on the normalized utilization across the partitions. If the normalized throughput exceeds 100% then the requests will be throttled. In this case, user can increase the autopilot max RUs. 
 
**Can the max RU value be increased on the container?**
<br>Yes max RUs can be increased to a higher value , but this is an asynchronous operation which will take some time, typically in the order of 4-6 hours. 
 
**Can the max RU value be decreased?**
<br>As long the storage in the container falls below the 0.01 * Max RUs, the reduction is allowed.  
 
**What is the number of allowed collections per database in a shared throughput model in autopilot?**
<br>Number of collections allowed is defined by this function = Min(25 , 0.001 * MaxRU)  



## **Recommended Documents**  

[Create Azure Cosmos containers and databases in autopilot mode (Preview)](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot)
<br>Azure Cosmos DB allows you to provision throughput on your containers in either manual or autopilot mode. This article describes the benefits and use cases of autopilot mode. In addition to manual provisioning of throughput, you can now configure Azure cosmos containers in autopilot mode. Azure Cosmos containers and databases configured in autopilot mode will automatically and instantly scale the provisioned throughput based on your application needs without compromising the SLAs.  

[Enable autopilot from Azure portal](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot#enable-autopilot-from-azure-portal)
<br>You can try out autopilot in your Azure Cosmos accounts by enabling in from Azure portal. Use the steps in this article to enable the autopilot option.