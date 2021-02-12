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

Server unavailability is caused by a restart and is usually temporary. A restart can happen for a number of reasons, such as: a service update is rolled out to your server and encounters a technical issue with the underlying infrastructure, or you unknowingly trigger a server restart by scaling the compute resources or by switching service tiers.

If the server continues to be unavailable for an extended period and after multiple connection attempts, this may be related to:
* Connection issues - review the "Error while connecting to server" content for help
* Long Postgres recovery time due to high transactional activity on the server at the time of restart


## **Recommended Steps**

* Try to reconnect to your server. If you can reconnect, consider [implementing retry logic](https://docs.microsoft.com/azure/postgresql/concepts-connectivity) to handle such transient errors and avoid application downtime.
* Check your server's **Resource health** to determine if any reported events on the service side may have caused the connection disruption
* Check the Postgres logs for additional insight
* If high resource utilization caused the restart, consider lowering utilization from connecting applications temporarily. In the future, consider setting alerts for rising resource utilization. Also, consider scaling up the server if this peak is likely to be reached again.

## **Recommended Documents**

* [Troubleshoot connection issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
