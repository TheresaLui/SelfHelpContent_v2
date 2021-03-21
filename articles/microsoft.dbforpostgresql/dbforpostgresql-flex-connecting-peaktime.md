<properties
    pageTitle="Connection issues during peak-time to PostgreSQL"
    description="Connection issues during peak-time to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32789523"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="84331719-f63c-41da-b181-1990065fe9c0"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **Error while connecting to server during workload peak hours**
## **Recommended Steps**

This means your connection string is correct and you can connect successfully during regular hours. However, during peak hours you are experiencing either connection failures or time outs. To address these, we recommend

- Check your active connections as well as CPU/memory/IO usage percentage in the portal metrics tab. High utilization may lead to unavailable resources for a new connection. Consider upgrading your server if the resource is reaching 100%.

- Check if all connections are actually used, or if some are idle. To check idle connections, query pg_stat_activity as described [Connection Handling blog](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Connection-handling-best-practice-with-PostgreSQL/ba-p/790883)
- If you receive the message "An existing connection was forcibly closed by the remote host", it indicates that your client closed the connection to the PostgreSQL server. Check your client timeout and idle connection settings. Learn more about [this error.](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/are-you-running-into-postgres-connection-issues-on-azure/ba-p/1994913).


## **Recommended Documents**

- [Quickstart: Connect and query with Azure CLI with Azure Database for PostgreSQL - Flexible Server](https://docs.microsoft.com/azure/postgresql/flexible-server/connect-azure-cli)
