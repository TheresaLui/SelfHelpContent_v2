<properties
	pageTitle="Performance and Query Execution/Unexpected increase in resource consumption"
	description="Performance and Query Execution/Unexpected increase in resource consumption"
	infoBubbleText="Performance and Query Execution/Unexpected increase in resource consumption"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637313"
	resourceTags=""	
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="37b18738-5961-46d2-b02e-ccbef09d471f"
	ownershipId="AzureData_AzureSQLMI"
/>

# Increase in resource consumption

To understand increase in resource consumption consider troubleshooting with monitoring tools that will help you identify the issue..

## **Recommended Steps**

To tune performance of database workloads, see [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview)

To help identify resource consumption, consider using the following options:

* Use Managed Instance overview through Azure portal for simple overview of CPU, IOPS and storage utilization
* For more advanced monitoring helping identify individual performance of queries, consider [Azure SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql)
* Consider using own DMV queries
* Consider using 3rd party solutions available for managed instance

## **Recommended Documents**

* [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview)
