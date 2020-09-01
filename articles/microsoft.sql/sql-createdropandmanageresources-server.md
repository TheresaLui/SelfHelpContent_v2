<properties
	pageTitle="create drop and manage resources/server"
	description="create drop and manage resources/server"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630453"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="88708ffa-27c8-477a-a193-e2616160b6e1"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# create drop and manage resources/server

## Move to Azure Resource Manager REST APIs for Azure SQL Database

Azure Resource Manager is our cloud infrastructure stack that fully replaces the classic Azure Service Manager deployment model. As a result, support for Service Manager REST APIs for Azure SQL Database will be retired on December 1, 2019. As with all changes of this type, we’re providing 12 months’ notice so you have adequate time to update your services that use Service Manager APIs for SQL Database to Resource Manager APIs. For more information see the [update announcement](https://azure.microsoft.com/updates/move-to-azure-resource-manager-rest-apis-for-azure-sql-database/) or for more details on the differences between Azure Resource Manager and Service Management see this [TechNet Blog article](https://secureinfra.blog/2016/12/22/difference-between-azure-service-manager-and-azure-resource-manager/).
Also see below for links to REST API Documentation for Server related operations in Azure Resource Manager.


**Capacity challenges and restrictions**

As demand continues to grow, we are faced with temporary capacity constraints in a number of Azure regions so we have established clear criteria for the priority of new cloud capacity. 

As mentioned in our commitment to customers and Microsoft cloud services continuity [here](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/), top priority is going to first responders, health and emergency management services, critical government infrastructure, and ensuring remote workers stay up and running with the core functionality. We will also constrain non-paid subscriptions as necessary, to ensure support of existing paid customers, so free trial & benefit subscriptions may see limited resource options and limited regions available.

If you would like assistance with this, please create a support request with our Quota team by following these [instructions](https://docs.microsoft.com/azure/sql-database/quota-increase-request).

**Blocked creating a server in a region**

If you are having troubles creating a server in a region and are seeing errors such as `'This location is not available for subscription'` in the Server create Portal blade, and you require assistance in obtaining access to that region please create a support request to the Quota team using these [instructions](https://docs.microsoft.com/azure/sql-database/quota-increase-request#other).

**Resource limit constraints**

If you are experiencing resource constraint limits related to:
- Max number of databases per server
- Max number of servers per subscription in any region
- Max number of Database transaction units (DTUs) per server
- Max number of vCores per server
- Max number of Elastic pools per server

See [here](https://docs.microsoft.com/azure/sql-database/sql-database-resource-limits-database-server) for more details on the default SQL database resource limits for a SQL Database server.

Please create a support request with our Quota team using these [instructions](https://docs.microsoft.com/azure/sql-database/quota-increase-request).

## **Recommended Documents**

* [What is an Azure SQL Database server](https://docs.microsoft.com/azure/sql-database/sql-database-servers)
* [Manage Azure SQL servers, databases, and firewalls using PowerShell](https://docs.microsoft.com/azure/sql-database/sql-database-servers#manage-azure-sql-servers-databases-and-firewalls-using-powershell)
* [Define server-level auditing policies](https://docs.microsoft.com/azure/sql-database/sql-database-auditing)<br>
* [SQL tools and utilities for Azure SQL Database](https://docs.microsoft.com/sql/tools/overview-sql-tools?view=sql-server-2017)
* [Create a server-level firewall rule for single and pooled databases using the Azure portal](https://docs.microsoft.com/azure/sql-database/sql-database-get-started-portal-firewall)
* [Create a single database in Azure SQL Database using the Azure Resource Manager template](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-get-started-template)

### **Rest API Documentation**
* [Servers REST API Documentation](https://docs.microsoft.com/rest/api/sql/servers)
