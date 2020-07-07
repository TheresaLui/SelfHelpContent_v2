<properties
    pageTitle="Server is currently not available"
    description="Server is currently not available"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="200"
    selfHelpType="generic"
    supportTopicIds="32639974"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6428cfa2-9135-430c-8f96-96c8768e01d1"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Database server is currently not available

Server unavailability is typically transient and due to a restart. A restart happens when a service update is rolled out to your server, a technical issue with the underlying infrastructure was encountered, you triggered a restart of the server, you scale the compute resources, or you change between service tiers.

If the server continues to be unavailable after a period and multiple connection attempts, this may be related to:
* Connection issues - please review the *Error while connecting to server* content for help
* Long Postgres recovery time due to high activity on the server at the time of restart


## **Recommended Steps**

* Try to reconnect to your server. If you can reconnect, consider [implementing retry logic](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) to handle such transient errors and avoid application downtime.
* Check **Resource health** for your server to see if there were any reported events on the service side that could have caused the connection disruption.
* Check the Postgres logs for additional insight
* If due to high resource utilization, consider temporarily lowering utilization from connecting applications. In the future, consider setting alerts for rising resource utilization. Also, consider scaling up the server if this peak is likely to be reached again.

## **Recommended Documents**

* [Troubleshoot connection issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
