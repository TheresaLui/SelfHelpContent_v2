<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32788703, 32789529"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d349d319-9ea5-411b-b348-6be7e235d9d2"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **Error while connecting to server during workload peak hours**
## **Recommended Steps**

This means your connection string is correct and you can connect successfully during regular hours. However, during peak hours you are experiencing either connection failures or time outs. To address these, we recommend

- Check your active connections as well as CPU/memory/IO usage percentage in the portal metrics tab. High utilization may lead to unavailable resources for a new connection. Consider upgrading your server if the resource is reaching 100%.
- Check the connection limit of your PostgreSQL server using [pricing tier](https://docs.microsoft.com/azure/postgresql/concepts-limits). The connection limits are published in the [documentation](https://docs.microsoft.com/azure/postgresql/concepts-limits).When connections exceed the limit, you may receive an error: `FATAL: sorry, too many clients already`.
- Check if all connections are actually used, or if some are idle. To check idle connections, query pg_stat_activity as described [Connection Handling blog](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Connection-handling-best-practice-with-PostgreSQL/ba-p/790883)
- If you receive the message "An existing connection was forcibly closed by the remote host", it indicates that your client closed the connection to the PostgreSQL server. Check your client timeout and idle connection settings. Learn more about [this error.](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/are-you-running-into-postgres-connection-issues-on-azure/ba-p/1994913).


## **Recommended Documents**

- [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
- [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
- [Understanding the connectivity architecture for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
