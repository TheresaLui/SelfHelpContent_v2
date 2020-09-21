<properties
	pageTitle="create drop and manage resources/elastic pools"
	description="create drop and manage resources/elastic pools"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa,andikshi"
    ms.author="emlisa,andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630419"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="88aaebf6-8c56-4b4b-807a-7ef2ca228385"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# create drop and manage resources/elastic pools

## **Recommended Steps**

There are several ways through which you can manage your elastic pools. If you are facing issues using one way please try an alternate approach. 
Elastic pools can be managed using:

* [Azure Portal](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-manage?WT.mc_id=pid%3A13491%3Asid%3A32630419%2F#azure-portal)
* [PowerShell](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-manage?WT.mc_id=pid%3A13491%3Asid%3A32630419%2F#powershell)
* [Azure CLI](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-manage?WT.mc_id=pid%3A13491%3Asid%3A32630419%2F#azure-cli)
* [T-SQL](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-manage?WT.mc_id=pid%3A13491%3Asid%3A32630419%2F#transact-sql-t-sql)
* [Rest-API](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-manage?WT.mc_id=pid%3A13491%3Asid%3A32630419%2F#rest-api)


## Adding database to elastic pool

If you are facing issues while adding the database to elastic pool, it could be due to the elastic pool reaching its storage limits. The following queries can be used to determine storage space quantities for an elastic pool. 

* [Query elastic pool for storage information](https://docs.microsoft.com/azure/azure-sql/database/file-space-manage#understanding-types-of-storage-space-for-an-elastic-pool)


## Capacity challenges and restrictions

As demand continues to grow, we are faced with temporary capacity constraints in a number of Azure regions so we have established clear criteria for the priority of new cloud capacity. 

As mentioned in our commitment to customers and Microsoft cloud services continuity [here](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/), top priority is going to first responders, health and emergency management services, critical government infrastructure, and ensuring remote workers stay up and running with the core functionality. We will also constrain non-paid subscriptions as necessary, to ensure support of existing paid customers, so free trial & benefit subscriptions may see limited resource options and limited regions available.

If you would like assistance with this, request you to please create a support request with our Quota team. You can do that by clicking on New Support request, then under the Basics tab select:
* Issue Type: Service and subscription limits (quotas)
* Quota type: SQL database

Please provide the following information when you submit the request: 
* Region: 
* Region need to be enabled? (Yes/No): 
* SKU (Example - B1M100/P1):
* No of Databases that will be deployed: (for SKU and number of databases, please let us know how many databases per SKU you need in case you need multiple SKUs)

## Move to Azure Resource Manager REST APIs for Azure SQL Database

Azure Resource Manager is our cloud infrastructure stack that fully replaces the classic Azure Service Manager deployment model. As a result, support for Service Manager REST APIs for Azure SQL Database will be retired on December 1, 2019. As with all changes of this type, we’re providing 12 months’ notice so you have adequate time to update your services that use Service Manager APIs for SQL Database to Resource Manager APIs. For more information see the [update announcement](https://azure.microsoft.com/updates/move-to-azure-resource-manager-rest-apis-for-azure-sql-database/) or for more details on the differences between Azure Resource Manager and Service Management see this [TechNet Blog article](https://secureinfra.blog/2016/12/22/difference-between-azure-service-manager-and-azure-resource-manager/).
Also see below for links to REST API Documentation for Elastic pool related operations in Azure Resource Manager.

## **Recommended Documents**
* [Overview of elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool?WT.mc_id=pid:13491:sid:32630419/)<br>
* [Elastic pools REST API](https://docs.microsoft.com/rest/api/sql/elasticpools?WT.mc_id=pid:13491:sid:32630419/)<br>
* [Scale elastic pool resources](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale?WT.mc_id=pid:13491:sid:32630419/)<br>
* [vCore-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-elastic-pools?WT.mc_id=pid:13491:sid:32630419/)<br>
* [DTU-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-elastic-pools?WT.mc_id=pid:13491:sid:32630419/)<br>

### **REST API Documentation**
* [Elastic pools REST API](https://docs.microsoft.com/rest/api/sql/elasticpools)
* [Azure SQL Management .NET SDK Library Microsoft.Azure.Management.Sql](https://www.nuget.org/packages/Microsoft.Azure.Management.Sql)