<properties
	pageTitle="Other"
	description="Other"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636814"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-other"
	displayOrder="244"
	category="Throughput and Scaling"
/>

# Throughput and Scaling Other Topics

Most users are able to resolve their Throughput issue using the steps below. 

## **Recommended Steps**  

### **Cannot find the option to enable Autopilot?**  
Autopilot has been registered for all users. Autopilot can only be enabled while creating new databases and containers from the Azure Portal.
- Support for CLI and SDK is not yet available
- Support to enable autopilot mode on existing containers and databases is not yet available

### **I am trying to create the tables programatically using ARM templates and cannot find the context for autopilot setting**
- Support for CLI and SDK is not yet available




## **Recommended Documents**

[Create Azure Cosmos containers and databases in autopilot mode (Preview)](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot)
<br>Azure Cosmos DB allows you to provision throughput on your containers in either manual or autopilot mode. This article describes the benefits and use cases of autopilot mode. In addition to manual provisioning of throughput, you can now configure Azure cosmos containers in autopilot mode. Azure Cosmos containers and databases configured in autopilot mode will automatically and instantly scale the provisioned throughput based on your application needs without compromising the SLAs.  

[Enable autopilot from Azure portal](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autopilot#enable-autopilot-from-azure-portal)
<br>You can try out autopilot in your Azure Cosmos accounts by enabling in from Azure portal. Use the steps in this article to enable the autopilot option.

* [Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
* [Provision throughput on containers and databases](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [How to distribute data globally with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
