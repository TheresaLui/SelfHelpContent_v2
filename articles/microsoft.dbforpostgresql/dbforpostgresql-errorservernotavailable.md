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

The "SSL SYSCALL error: EOF detected" message or other connection errors occur when the PostgreSQL server is restarting. A restart can occur when a service update was rolled out to your server, a technical issue was encountered, or you changed the compute resources or service tier of the server. The error you are seeing are transient and generally go away in less than 60 seconds.

Applications that are connecting to cloud services [should implemented retry logic](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) to catch handle such transient errors.

## **Recommended documents**

[Troubleshoot connection issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
