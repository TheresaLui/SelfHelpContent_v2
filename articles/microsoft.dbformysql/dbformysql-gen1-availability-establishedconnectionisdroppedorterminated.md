<properties
    pageTitle="Connection issues for Azure Database for MySQL Flexible Server"
    description="Connection issues for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32747561"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="4c19b79f-072a-4b30-a3d3-0abc6610f8a9"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Dropped connections

An established connection to an Azure Database for MySQL Single server can be terminated for multiple reasons, including client connection timeouts, changes to the server configuration, network failures, server restarts, and so on. Please work through the steps below for a first level of troubleshooting your connection issue.

## **Recommended Steps**

* Try to reconnect to your server. If you are able to reconnect, please switch to the problem subtype *Error while connecting to server* to troubleshoot intermittent connection problems.
* Check the **Resource health** for your server to see if there were any reported events that could have caused the connection disruption
* Check the **Activity log** for your server to see if there are changes to the server that could have causes the connection drops
* Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your client's timeout settings.


## **Recommended Documents**

*   [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
*   [Tutorial: Creating and connecting to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal)