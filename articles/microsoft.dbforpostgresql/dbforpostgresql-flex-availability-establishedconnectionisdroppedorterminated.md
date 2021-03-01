<properties
    pageTitle="Connection issues to Azure Database for PostgreSQL"
    description="Connection issues to Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="rachel-msft"
    ms.author="raagyema"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32780960"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-availability-establishedconnectionisdroppedorterminated"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Dropped connections

An established connection to an Azure Database for PostgreSQL server can be terminated for multiple reasons, including client connection timeouts, changes to the server configuration, network failures, server restarts, and so on. For the first level of troubleshooting your issue, Work through the following steps.

## **Recommended Steps**

* Try to reconnect to your server. If you are able to reconnect, switch to the problem subtype *Error while connecting to server* to troubleshoot intermittent connection problems.
* Check the **Activity log** for your server to see if there are changes to the server that cause the connection drops
* Check the Postgres logs to see if there was a restart
* Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, review your client's timeout settings.

