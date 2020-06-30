<properties
	pageTitle="How-To: Azure SQL Database Management"
	description="How-To: Azure SQL Database Management"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa, johirsch,andikshi"
    ms.author="emlisa,andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630418"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="29427fe7-6a8b-46fc-aa6d-8d3fd5176098"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# How-To: Azure SQL Database Management

## Move to Azure Resource Manager REST APIs for Azure SQL Database

Azure Resource Manager is our cloud infrastructure stack that fully replaces the classic Azure Service Manager deployment model. As a result, support for Service Manager REST APIs for Azure SQL Database will be retired on December 1, 2019. As with all changes of this type, we’re providing 12 months’ notice so you have adequate time to update your services that use Service Manager APIs for SQL Database to Resource Manager APIs. For more information see the [update announcement](https://azure.microsoft.com/updates/move-to-azure-resource-manager-rest-apis-for-azure-sql-database/) or for more details on the differences between Azure Resource Manager and Service Management see this [TechNet Blog article](https://secureinfra.blog/2016/12/22/difference-between-azure-service-manager-and-azure-resource-manager/).
Also see below for links to REST API Documentation for Database related operations in Azure Resource Manager.

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

### Databases created in Gen5 tier rather than S0 when tier isn't specified
The default SLO for new databases has switched from S0 to GP_Gen5_2. Using T-SQL, Entity Framework, PowerShell, or AzureCLI to create a database without specifying a service tier will now result in provisioning a GP_Gen5_2 database. Any automated means of creating new databases that do not specify the service tier will now behave differently in terms of the performance and pricing of the newly created databases. For more information, see the [update announcement](https://azure.microsoft.com/updates/azure-sql-database-default-configuration-changing-soon/).

### Shrink database by clearing up unused space
* To free up space and shrink log files, use [these console commands](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-shrinkdatabase-transact-sql)

### Trouble dropping a database through Azure Portal

Often, when dropping a database using Azure Portal fails, dropping the database using SQL Server Management Studio will work more reliably. To do this, run "DROP [database name](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query-ssms)" from SSMS.

### Trouble creating a database in Central Australia

Subscription whitelisting is required for provisioning new databases in the Central Australia region. File a request for whitelisting [here](https://azure.microsoft.com/global-infrastructure/australia/contact/).

## **Recommended Documents**
* [What is Azure SQL Database?](https://docs.microsoft.com/azure/azure-sql/database/sql-database-paas-overview)
* [Change database name, edition, size and other options](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630418/)<br>
* [Managing Azure SQL Databases using the Azure portal](https://azure.microsoft.com/documentation/articles/sql-database-manage-portal?WT.mc_id=pid:13491:sid:32630418/)

### **REST API Documentation**
* [Databases REST API](https://docs.microsoft.com/rest/api/sql/databases)
* [Azure SQL Management .NET SDK Library Microsoft.Azure.Management.Sql](https://www.nuget.org/packages/Microsoft.Azure.Management.Sql)