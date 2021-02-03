<properties
    pageTitle="Slow query logs in Azure Database for MySQL Single Server"
    description="Slow query logs in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="210"
    selfHelpType="generic"
    supportTopicIds="32747588"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c30174c2-3ede-4f21-ba92-59a3fd36fb3d"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Slow query logs in Azure Database for MySQL Single Server

Azure Database for MySQL Single Server offers [slow query logs](https://docs.microsoft.com/azure/mysql/concepts-server-logs) that can be used to identify slow running queries and assist with performance troubleshooting.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Enabling slow query logs*

Slow query logs are disabled by default. Use the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli) to enable logs.

*Configuring slow query logs*

* Logging behavior can be changed using a number of server parameters (ex. **`long_query_time`**). Refer to the [slow query logs documentation](https://docs.microsoft.com/azure/mysql/concepts-server-logs) for the full list.
* If your tables are not indexed, setting the **`log_queries_not_using_indexes`** and **`log_throttle_queries_not_using_indexes`** parameters to ON may affect MySQL performance since all queries running against these non-indexed tables will be written to the slow query log

*Accessing slow query logs*

* There are two ways slow query logs can be consumed: .log files or Azure Monitor diagnostic settings (which routes to storage account, Event Hub, or Azure Monitor logs)
    * .log files provide short-term storage for logs in a CSV-like format and are stored locally on the server. These logs are retained for up to seven days and the files are rotated every 24 hours or 7 GB (whichever comes first). They can be downloaded from the Azure portal (Server logs page) or CLI.
    * Diagnostic logs send logs in JSON format to Azure Monitor logs, Event Hubs, or Azure Storage for longer term storage and analysis. This feature is only available in the General Purpose and Memory Optimized pricing tiers. Use your server's **Diagnostic settings** page in the Azure portal to configure where to emit your logs to using the "MySqlSlowLogs" log type.
    * The **`log_output`** parameter allows you to configure where logs are output to. If "File", the slow query log is written to both the local server storage and to Azure Monitor diagnostics. If "None", the slow query log will only be written to Azure Monitor diagnostics.
* If you are downloading large slow query log files from the Azure portal, you may want to consider using a download manager to increase the threads available to download

## **Recommended Documents**
* [Slow query logs](https://docs.microsoft.com/azure/mysql/concepts-server-logs)<br>
* [Configure slow query logs - Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal)<br>
* [Configure slow query logs - Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli)