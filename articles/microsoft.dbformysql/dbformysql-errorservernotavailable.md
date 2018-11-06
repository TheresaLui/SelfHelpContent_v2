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
The "Can't connect to MySQL server on.." message or other connection errors occurs when the MySQL server has been restarted because of deployment, failover, scaling or load balancing. This is a transient connectivity issue as reconfigurations are generally expected to complete in less than 60 seconds.

Applications that are connecting to cloud services [should be coded](https://docs.microsoft.com/azure/mysql/concepts-high-availability#application-retry-logic-is-essential) to catch periodic connection errors and should implement retry logic.<br>

## **Recommended documents**
* [Troubleshoot Database unavailability related errors](https://docs.microsoft.com/azure/mysql/concepts-high-availability)
