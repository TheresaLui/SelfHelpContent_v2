<properties
	pageTitle="Error: Database 'x' on server 'y' is not currently available"
	description="Error: Database 'x' on server 'y' is not currently available"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servers, databases"
	productPesIds=""
	cloudEnvironments="public"
/>

# Error: Database 'x' on server 'y' is not currently available

## **Recommended steps**
The "unable to connect" message (error code 40613) occurs when the Azure SQL Database has been moved because of deployment, failover, or load balancing. This is a transient connectivity issue because reconfigurations are generally expected to complete in less than 60 seconds.

* Applications that are connecting to cloud services should be coded to catch periodic connection errors (e.g., 40613) and should implement retry logic.<br>
[Retry logic for transient errors](https://azure.microsoft.com/documentation/articles/sql-database-connectivity-issues/#retry-logic-for-transient-errors)

## **Recommended documents**
[Troubleshoot "Database x on server y is not currently available. Please retry the connection later."](https://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-connection)
