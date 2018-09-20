<properties
	pageTitle="Your SQL database is unavailable due to reconfigurations"
	description="SQL Reconfigurations"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.sql"
	resource="server/database"
	authors="aamalvea"
	articleId="servicehealthinsights-microsoft.sql-server/database-healthannotation_sql_reconfigurations_standard"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_sql_reconfigurations_standard"
/>

# Your SQL database is unavailable due to reconfigurations

We're sorry. Your SQL database, <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> due to reconfiguration.

The Azure infrastructure has the ability to dynamically reconfigure servers when heavy workloads arise in the SQL Database service. This dynamic behavior might cause your client program to lose its connection to SQL Database. This kind of error condition is called a transient fault and usually takes less than 60 seconds.

## **Recommended steps**

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

* [To avoid the connection issues caused by Azure configurations in the future, you have to implement retry logic in your code](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-connectivity-issues#transient-errors-transient-faults)
