<properties
	pageTitle="Error: Server not available"
	description="Error: Server not available or SSL SYSCALL error: EOF detected"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="ankam"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32628435, 32628434"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
/>

# Error: Server not available or SSL SYSCALL error: EOF detected

## **Recommended steps**
The "SSL SYSCALL error: EOF detected" message or connection errors occurs when the Postgres server has been restarted because of deployment, failover, scaling or load balancing. This is a transient connectivity issue as reconfigurations are generally expected to complete in less than 60 seconds.

Applications that are connecting to cloud services [should be coded](https://docs.microsoft.com/azure/postgresql/concepts-high-availability#application-retry-logic-is-essential) to catch periodic connection errors and should implement retry logic.<br>

## **Recommended documents**
* [Troubleshoot Database unavailability related errors](https://docs.microsoft.com/azure/postgresql/concepts-high-availability)
