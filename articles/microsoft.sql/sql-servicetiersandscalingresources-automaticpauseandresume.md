<properties
	pageTitle="Automatic pause and resume(SQL DB Serverless)"
	description="Automatic pause and resume(SQL DB Serverless)"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
    ms.author="andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639119"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="sql-servicetiersandscalingresources-automaticpauseandresume"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# Issues for SQL DB Serverless

Serverless is price-performance optimized for single databases with intermittent, unpredictable usage patterns that can afford some delay in compute warm-up after idle usage periods. In contrast, the provisioned compute tier is price-performance optimized for single databases or multiple databases in elastic pools with higher average usage that cannot afford any delay in compute warm-up.<br>

Scenarios well-suited for serverless compute:

* Single databases with intermittent, unpredictable usage patterns interspersed with periods of inactivity and lower average compute utilization over time
* Single databases in the provisioned compute tier that are frequently rescaled and customers who prefer to delegate compute rescaling to the service
* New single databases without usage history where compute sizing is difficult or not possible to estimate prior to deployment in SQL Database

Scenarios currently not supported:

Enabling auto-pause for a serverless database is not supported if long-term retention (LTR) is enabled.

## **Recommended Documents**

* [Serverless Overview](https://docs.microsoft.com/azure/sql-database/sql-database-serverless)<br>
* [Resource limits for serverless](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases#general-purpose---serverless-compute---gen5)

