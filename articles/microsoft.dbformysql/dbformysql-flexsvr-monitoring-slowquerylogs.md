<properties
    pageTitle="Slow query logs in Azure Database for MySQL Flexible Server"
    description="Slow query logs in Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="220"
    selfHelpType="generic"
    supportTopicIds="32747640"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="51d12b41-62ef-431d-8789-73f51a2c4222"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Slow query logs in Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible Server offers [slow query logs](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-slow-query-logs) that can be used to identify slow running queries and assist with performance troubleshooting.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Enabling slow query logs*

Slow query logs are disabled by default. Use the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-configure-slow-query-logs-portal) or Azure CLI to enable logs.

*Configuring slow query logs*

* Logging behavior can be changed using a number of server parameters (ex. **`long_query_time`**). Refer to the [slow query logs documentation](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-slow-query-logs) for the full list.
* If your tables are not indexed, setting the **`log_queries_not_using_indexes`** and **`log_throttle_queries_not_using_indexes`** parameters to ON may affect MySQL performance since all queries running against these non-indexed tables will be written to the slow query log

*Accessing slow query logs*

* Slow query logs are integrated with Azure Monitor diagnostics. This allows your logs (in JSON format) to be emitted to Azure Monitor logs, Event Hubs, or Azure Storage for longer term storage and analysis.
* Use your server's **Diagnostic settings** page in the Azure portal to configure where to emit your logs to using the "MySqlSlowLogs" log type
* Refer to the [slow query logs](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-slow-query-logs#access-slow-query-logs) documentation to learn more about log analysis and output

## **Recommended Documents**
* [Slow query logs](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-slow-query-logs)
* [Configure slow query logs - Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-configure-slow-query-logs-portal)