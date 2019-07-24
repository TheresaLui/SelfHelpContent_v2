<properties
    pageTitle="Connection issues to MariaDB"
    description="Connection issues to MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="40"
    selfHelpType="resource"
    supportTopicIds="32640120"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="61fd6b3b-9706-4eeb-9f56-4bc956116579"
/>

# Connection issues to Azure Databases for MariaDB

An established connection to an Azure Database for MariaDB server can be terminated for multiple reasons, including client connection timeouts, changes of the server configuration, network failures, server restarts, and so on. Please work through the step below for a first level of troubleshooting your connection issue.

## **Recommended Steps**

* Try to reconnect to your server. If you are not able to reconnect, please switch to the problem subtype *Database is currently unavailable* to troubleshoot intermittent connection problems.
* Check the **Resource health** for your server to see if there were any reported events that could have caused the connection disruption
* Check the **Activity log** for you database to see if there changes to the server that could have causes the connection drops
* Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your setting for the following server parameters: *connect_timeout*, *wait_timeout*, and *interactive_timeout*. Consult the MariaDB documentation for current server version for more information.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
