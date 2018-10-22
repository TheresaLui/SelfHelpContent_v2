<properties
	pageTitle="query execution/unexpected behavior"
	description="query execution/unexpected behavior"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
	displayOrder="6"
	selfHelpType="generic"
	supportTopicIds="31980438"
	resourceTags="databases, servers"
	productPesIds="13491"
	cloudEnvironments="public"
/>

# query execution/performance and time outs

## **Recommended steps**

* Poor performance in Azure SQL DB is most often either related to excessive CPU utilization or a query waiting on a resource.  The following reference walks through how to address both troubleshooting paths: [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview/)<br>

* For connection errors and transient errors that your client application encounters when it interacts with Azure SQL Database, the following reference covers how to prevent, troubleshoot, diagnose and mitigate such errors: [Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues/)