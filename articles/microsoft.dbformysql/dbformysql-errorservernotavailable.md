<properties
	pageTitle="Error: Server not available"
	description="Error: Server not available detected"
	service="microsoft.dbformysql"
	resource="servers"
	authors="ankam"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32628385"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
/>

# Error: Server not available

## **Recommended steps**

The "Can't connect to MySQL server on.." message or other connection errors occur when the MySQL server is restarting. A restart can occur when a service update was rolled out to your server, a technical issue was encountered, or you changed the compute resources or service tier of the server. The error you are seeing is transient and generally goes away in less than 60 seconds.

Applications that are connecting to cloud services [should implement retry logic](https://docs.microsoft.com/azure/mysql/concepts-connectivity) to handle such transient errors.

## **Recommended documents**

[Troubleshoot connection issues to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
