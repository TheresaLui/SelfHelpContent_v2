<properties
	pageTitle="Error: Server not available"
	description="Error: Server not available or SSL SYSCALL error: EOF detected"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="ankam"
    ms.author="ankam,janeng"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32628435, 32628434, 32628436, 32639974, 32639979"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="e0349317-477d-4dd6-bada-7a2d78d09118"
/>

# Error: Server not available or SSL SYSCALL error: EOF detected

The "SSL SYSCALL error: EOF detected" message or other connection errors occur when the PostgreSQL server is restarting. A restart can occur when a service update was rolled out to your server, a technical issue was encountered, or you changed the compute resources or service tier of the server. The error you are seeing is transient and generally goes away in less than 60 seconds.

## **Recommended Steps**

* Applications that are connecting to cloud services [should implement retry logic](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) to handle such transient errors

## **Recommended Documents**

* [Troubleshoot connection issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
