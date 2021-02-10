<properties
	pageTitle="sql-servicetiersorscalingresources/purchasing models (DTU, vCore, reserved capacity, etc)"
	description="sql-servicetiersorscalingresources/purchasing models (DTU, vCore, reserved capacity, etc)"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
    ms.author="andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632131"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="sql-servicetiersorscalingresources-purchasingmodels"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# create drop and manage resources/purchasing models (DTU, vCore, reserved capacity, etc)

[[_TOC_]]

** If you have already tried to scale a database or elastic pool and are facing issues (operation is long running , stuck , or have general questions), please go back to the Previous:Basics tab and select the Problem subtype(last drop down) to be Issues scaling a database or elastic pool. **

[Goto](button-data-blade:<button-data-blade:Microsoft_Azure_Classic_Compute.PasswordResetBlade.assetId.$resourceId>)

## Moving between service tiers

You can easily convert your database to any supported performance objective (DTU to VCore and visa versa) by using the Azure portal, PowerShell, the Azure CLI, T-SQL, or the REST API. You don't need to take the application offline. The service tiers offer a simple online-conversion method that's similar to the existing process of upgrading databases from the standard to the premium service tier and the other way around.

See [Manage single databases](https://docs.microsoft.com/azure/azure-sql/database/single-database-scale) and [Manage elastic pools](https://docs.microsoft.com/azure/azure-sql/database/single-database-scale).

## Pricing and cost analysis

* For more information on pricing visit the [pricing](https://azure.microsoft.com/pricing/details/sql-database/single/) page.
* Azure Cost Management helps you set budgets and configure alerts to keep spending under control. Analyze, manage, and optimize your costs with Cost Management. To learn more, see the [quickstart on analyzing your costs](https://docs.microsoft.com/azure/cost-management-billing/costs/quick-acm-cost-analysis?tabs=azure-portal).

### Automate management of databases

You can define target database or groups of databases where the job will be executed, and also define schedules for running a job. A job handles the task of logging in to the target database. You also define, maintain, and persist Transact-SQL scripts to be executed across a group of databases.
Every job logs the status of execution and also automatically retries the operations if any failure occurs. For further details follow [Automation](https://docs.microsoft.com/azure/azure-sql/database/job-automation-overview) 

### Quota Requests

To request a quota increase or whitelist a subscription for a particular region follow [Quota requests](https://docs.microsoft.com/azure/azure-sql/database/quota-increase-request)

### Problems selecting a particular service tier

If you are facing issues while choosing a particular service tier, it could be due to: 

### 1. Capacity issues 

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

### 2. Portal issues 

	If you are unable to view the database in your Azure portal but are still able to view\manage it using other client tools, it could be a issue with browser cache, we recommend:
	* Trying incognito or private mode in the browser. 
	* Clear your browser cache. 
	* Re-login into your portal.

### Choosing between service tiers

* DTU-based

	This model is best for  Customers who want simple, preconfigured resource options. It is based on a bundled measure of compute, storage, and I/O resources. Compute sizes are expressed in DTUs for single databases and in elastic database transaction units (eDTUs) for elastic pools. For more information about DTUs and eDTUs, see [What are DTUs and eDTUs?](https://docs.microsoft.com/azure/azure-sql/database/purchasing-models#dtu-based-purchasing-model).	

* vCore-based
		This model is best for Customers who value flexibility, control, and transparency. It allows you to independently choose compute and storage resources. The vCore-based purchasing model also allows you to use [Azure Hybrid Benefit](https://azure.microsoft.com/pricing/hybrid-benefit/) for SQL Server to save costs.

## **Recommended Documents**

* [Overview of purchasing models](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers?WT.mc_id=pid:13491:sid:32630449/)
* [vCore-based model](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-vcore?WT.mc_id=pid:13491:sid:32630449/)
* [DTU-based service tiers](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32630449/)
* [Prepay for reserved capacity](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32630449/)
