<properties
    pageTitle="Connection issues to Azure Databases for PostgreSQL"
    description="Connection issues to Azure Databases for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32731217"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2393642e-b8d9-413e-be03-8535589ccc46"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Dropped connections

An established connection to an Azure Database for PostgreSQL server can be terminated for multiple reasons, including client connection timeouts, changes to the server configuration, network failures, server restarts, and so on. Please work through the steps below for a first level of troubleshooting your connection issue.

## **Recommended Steps**

* Try to reconnect to your server. If you are able to reconnect, please switch to the problem subtype *Error while connecting to server* to troubleshoot intermittent connection problems.
* Check the **Resource health** for your server to see if there were any reported events that could have caused the connection disruption
* Check the **Activity log** for your server to see if there are changes to the server that could have causes the connection drops
* Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your client's timeout settings.


## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
