<properties
    pageTitle="Slow query logging capabilities in Azure Database for MySQL"
    description="Slow query logging capabilities in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="480"
    selfHelpType="generic"
    supportTopicIds="32730382"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1086df0a-65e8-428f-8e7d-4ef9b9a19927"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Slow query logs in Azure Database for MySQL

Azure Database for MySQL Single Server and Flexible Server offer slow query logs that can be used to identify slow running queries and assist with performance troubleshooting.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Enabling slow query logs*

Slow query logs are disabled by default. Use the following to enable logs:
* Azure portal: [Single server](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) | [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-configure-slow-query-logs-portal)
* Azure CLI: [Single server](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli)

*Configuring slow query logs*

* Logging behavior can be changed using a number of server parameters (ex. **`long_query_time`**). Refer to the [slow query logs documentation](https://docs.microsoft.com/azure/mysql/concepts-server-logs) for the full list.
* If your tables are not indexed, setting the **`log_queries_not_using_indexes`** and **`log_throttle_queries_not_using_indexes`** parameters to ON may affect MySQL performance since all queries running against these non-indexed tables will be written to the slow query log

*Accessing slow query logs*

* In single server, slow query logs are available via downloadable log files or integration with Azure Monitor diagnostics. This behavior is set using the **`log_output`** parameter.
* In flexible server, logs are integrated with Azure Monitor diagnostics, which emits logs (in JSON format) to a storage account, Event Hub, or Azure Monitor logs for longer term storage and analysis

## **Recommended Documents**

* [Single server - Slow query logs](https://docs.microsoft.com/azure/mysql/concepts-server-logs)<br>
* [Flexible server - Slow query logs](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-slow-query-logs)