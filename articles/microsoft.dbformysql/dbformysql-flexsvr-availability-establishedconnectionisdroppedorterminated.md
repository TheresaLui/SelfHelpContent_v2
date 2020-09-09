<properties
    pageTitle="Connection issues for Azure Database for MySQL Flexible Server"
    description="Connection issues for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="130"
    selfHelpType="generic"
    supportTopicIds="32747614"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e920dc8b-22f6-42be-bedd-34abfb2591c2"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Dropped connections

An established connection to an Azure Database for MySQL Flexible server can be terminated for multiple reasons, including client connection timeouts, changes to the server configuration, network failures, server restarts, and so on. Please work through the steps below for a first level of troubleshooting your connection issue.

## **Recommended Steps**

* Try to reconnect to your server. If you are able to reconnect, please switch to the problem subtype *Error while connecting to server* to troubleshoot intermittent connection problems.
* Check the **Resource health** for your server to see if there were any reported events that could have caused the connection disruption
* Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your client's timeout settings.


## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL Flexible server](https://docs.microsoft.com/azure/mysql/flexible-servers/erverhow-to-troubleshoot-common-connection-issues)<br>
* [Tutorial: Creating and connecting to Azure Database for MySQL Flexible server](https://docs.microsoft.com/azure/mysql/flexible-servers/quickstart-create-server-portal)
