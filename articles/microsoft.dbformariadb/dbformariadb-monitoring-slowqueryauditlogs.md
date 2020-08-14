<properties
    pageTitle="Slow query and audit logging capabilities in Azure Database for MariaDB"
    description="Slow query and audit logging capabilities in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="450"
    selfHelpType="generic"
    supportTopicIds="32731922"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1086df0a-65e8-428f-8e7d-dfd76741b8987"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Slow query and audit logging capabilities in Azure Database for MariaDB

Azure Database for MariaDB has slow query and audit logs available. Slow query logs can be used to identify slow running queries and audit logs can be used to audit database events.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Slow query logs*

* Review documentation about [slow query logs](https://docs.microsoft.com/azure/mariadb/concepts-server-logs)
* Review how to configure & access slow query logs from the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-configure-server-logs-portal) and [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-logs-cli)
* If your tables are not indexed, setting the **log_queries_not_using_indexes** and **log_throttle_queries_not_using_indexes** parameters to ON may affect MariaDB performance since all queries running against these non-indexed tables will be written to the slow query log.
* There are two ways slow query logs can be consumed: .log files or Azure Monitor diagnostic logging (which routes to storage account, Event Hub, or Azure Monitor logs)
  * .log files provide short-term storage for logs in a CSV-like format and are stored locally on the server. These logs are retained for up to seven days and the files are rotated every 24 hours or 7 GB (whichever comes first). They can be downloaded from the Azure portal or CLI
  * Diagnostic logs send logs in JSON format to a storage account, Event Hub, or Azure Monitor logs for longer term storage and analysis. This feature is only available in the General Purpose and Memory Optimized pricing tiers
  * The **log_output** parameter allows you to configure where logs are output to. If "File",  the slow query log is written to both the local server storage and to Azure Monitor Diagnostic Logs. If "None", the slow query log will only be written to Azure Monitor Diagnostics Logs.
* If you are downloading large slow query log files from the Azure portal, you may want to consider using the [Microsoft Download Manager](https://www.microsoft.com/en-us/download/details.aspx?id=27960) to increase the threads available to download.

*Audit logs*

* Review documentation about [audit logs](https://docs.microsoft.com/azure/mariadb/concepts-audit-logs)
* Review how to configure logs from the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-configure-audit-logs-portal)
* Audit logs are only available through Azure Monitor diagnostic logging (which routes to storage account, Event Hub, or Azure Monitor logs)
* It is recommended to only log the event types (using the **audit_log_events** parameter) and users (using the **audit_log_include_users** & **audit_log_exclude_users** parameters) required for your auditing purposes to ensure your server's performance is not heavily impacted.

## **Recommended Documents**

* [Access slow query logs - Portal](https://docs.microsoft.com/azure/mariadb/howto-configure-server-logs-portal)<br>
* [Access slow query logs - CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-server-logs-cli)<br>
* [Configure and access audit logs - Portal](https://docs.microsoft.com/azure/mariadb/howto-configure-audit-logs-portal)<br>
* [Configure and access audit logs - CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-audit-logs-cli)
