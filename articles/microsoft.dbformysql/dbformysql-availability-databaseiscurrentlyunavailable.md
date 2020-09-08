<properties
    pageTitle="Connection issues to Azure Databases for MySQL"
    description="Connection issues to Azure Databases for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="20"
    selfHelpType="generic"
    supportTopicIds="32640051"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ee0be1b6-1669-4826-a848-039ae852d786"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Error: Server not available

The "Can't connect to MySQL server on.." message, dropped connections, and other transient connection errors can occur when your MySQL server is restarting. A restart happens when a service update is rolled out to your server, a technical issue with the underlying infrastructure was encountered, you triggered a restart of the server, you changed the compute resources, or you change between service tiers. The error you are seeing is transient and generally goes away in less than 60 seconds.

## **Recommended Steps**

* Try to reconnect to your server. If you can reconnect, consider [implementing retry logic](https://docs.microsoft.com/azure/mysql/concepts-connectivity) to handle such transient errors and avoid application downtime.
* If your server is crashing and restarting, please review the **Memory Percent** metric in the Metrics blade in the portal. If you see the usage of **Memory Percent** is low, this can be because the server ran out of commit memory and not working set memory. We recommend to consider reducing **innodb_buffer_pool_size** to release some memory.
* If the server is in read-only mode, please either increase the storage size using the portal as described in [reaching storage limit](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#reaching-the-storage-limit) or enable storage **auto-growth**.Review [How to enable storage auto-growth](https://docs.microsoft.com/azure/mysql/howto-auto-grow-storage-portal#enable-storage-auto-grow).
* Check the resource health for your server to see if there were any reported events on the service side that could have caused the connection disruption.
* If the **Resource health** for your server is not indicating any disruptions, consider the troubleshooting steps outline in the problem subtopic *Error while connecting to the server*.

## **Recommended Documents**

* [Troubleshoot connection issues to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
