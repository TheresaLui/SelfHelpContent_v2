<properties
    pageTitle="Connection issues to MySQL"
    description="Connection issues to MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="40"
    selfHelpType="resource"
    supportTopicIds="32640055"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="cf53cc8b-732f-4262-b101-f8eab4930254"
/>

# Connection issues to Azure Databases for MySQL

An established connection to an Azure Database for MySQL server can be terminated for multiple reasons, including client connection timeouts, changes of the server configuration, network failures, server restarts, and so on. Please work through the step below for a first level of troubleshooting your connection issue.

## **Recommended Steps**

* Try to reconnect to your server. If you are not able to reconnect, please switch to the problem subtype *Database is currently unavailable* to trouble shoot intermitted connection problems.
* Check the **Rresource health** for your server to see if there were any reported events that could have caused the connection disruption
* Check the **Activity log** for you database to see if there changes to the server that could have causes the connection drops
* Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your setting for the following server parameters: *connect_timeout*, *wait_timeout*, and *interactive_timeout*. Consult the MySQL documentation for current server version for more information.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
