<properties
	pageTitle="How to questions related to performance issues in Azure SQL Database"
	description="How to questions related to performance issues in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749516"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    	resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-howtoquestions"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# How to questions related to performance issues in Azure SQL Database

## Choosing the right service tier

If you are new to Azure SQL Database and are seeking guidance on choosing the right service tier, see [Choosing the Right Database Reservation Size](https://techcommunity.microsoft.com/t5/sql-customer-success-engineering/azure-sql-db-design-note-choosing-the-right-database-reservation/ba-p/872825).
If you have decided to go with a DTU-based model and are not able to identify the right DTU value, see the [DTU Calculator](https://dtucalculator.azurewebsites.net/).

## Partition the database

In many large-scale solutions, data is divided into partitions that can be managed and accessed separately. Partitioning can improve scalability, reduce contention, and optimize performance. It can also provide a mechanism for dividing data by usage pattern. For example, you can archive older data in cheaper data storage. See the [Database Partitioning Guide](https://docs.microsoft.com/azure/architecture/best-practices/data-partitioning) for more details.

## SLA for various service tiers

Azure SQL Database is a fully managed relational database with built-in regional high availability and turnkey geo-replication to any Azure region. See [Azure SQL Database SLA](https://azure.microsoft.com/support/legal/sla/sql-database/v1_4/) for terms and further details on SLA.

## Elastic queries

The elastic query feature (in preview) enables you to run a Transact-SQL query that spans multiple databases in Azure SQL Database. It lets you perform cross-database queries to access remote tables, and to connect Microsoft and third-party tools (Excel, Power BI, Tableau, and so on) to query across data tiers with multiple databases. Using this feature, you can scale out queries to large data tiers and visualize the results in business intelligence (BI) reports. See [Azure SQL Database elastic query overview (preview)](https://docs.microsoft.com/azure/azure-sql/database/elastic-query-overview) for more details.

## **Recommended Documents**

* Poor performance in Azure SQL DB is usually related to excessive CPU utilization or to a query waiting for a resource. To resolve either of these issues, see [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview?WT.mc_id=pid:13491:sid:32630450/).
* Follow [Overview of Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/sql-database-paas-overview) to understand more about the product.
* Follow [Azure SQL Database documentation](https://docs.microsoft.com/azure/azure-sql/database/) to get more details on the features and common issues.

