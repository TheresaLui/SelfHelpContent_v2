<properties
	pageTitle="Error: Server not available"
	description="Error: Server not available detected"
	service="microsoft.dbformariadb"
	resource="servers"
	authors="ajlam"
    ms.author="andrela"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32640117,32640120"
	resourceTags="servers, databases"
	productPesIds="16617"
	cloudEnvironments="public"
	articleId="mariadbserverunavailable"
/>

# Error: Server not available

The "Can't connect to MariaDB server on.." message or other connection errors occur when the MariaDB server is restarting. A restart can occur when a service update was rolled out to your server, a technical issue was encountered, or you changed the compute resources or service tier of the server. The error you are seeing is transient and generally goes away in less than 60 seconds.

## **Recommended Steps**

* Applications that are connecting to cloud services [should implement retry logic](https://docs.microsoft.com/azure/mariadb/concepts-connectivity) to handle such transient errors

## **Recommended Documents**

* [Troubleshoot connection issues to Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
