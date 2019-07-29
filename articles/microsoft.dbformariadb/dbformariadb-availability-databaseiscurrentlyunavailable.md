<properties
    pageTitle="Connection issues to Azure Databases for MariaDB"
    description="Connection issues to Azure Databases for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="20"
    selfHelpType="resource"
    supportTopicIds="32640117"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="b6543926-97c4-479c-8443-e42a2011c7db"
/>

# Error: Server not available

The "Can't connect to MariaDB server on.." message, dropped connections, and other transient connection errors can occur when the your MariaDB server is restarting. A restart happens when a service update is rolled out to your server, a technical issue with the underlying infrastructure was encountered, you triggered a restart of the server, you changed the compute resources, or you change between service tiers. The error you are seeing is transient and generally goes away in less than 60 seconds.

## **Recommended Steps**

* Try to reconnect to your server. If you can reconnect, consider [implementing retry logic](https://docs.microsoft.com/azure/mariadb/concepts-connectivity) to handle such transient errors and avoid application downtime.
* Check the resource health for your server to see if there were any reported events on the service side that could have caused the connection disruption
* If the **Resource health** for your server is not indicating any disruptions, consider the troubleshooting steps outline in the problem subtopic *Error while connecting to the server*

## **Recommended Documents**

* [Troubleshoot connection issues to Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
