<properties
    pageTitle="Auditing capabilities in Azure Database for MySQL"
    description="Auditing capabilities in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32640045"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax"
    articleId="1086df0a-65e8-428f-8e7d-4ef9b9a19924"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Monitoring server logs

Azure Database for MySQL has slow query and audit logs available. Slow query logs can be used to identify slow running queries and audit logs can be used to audit database events.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Slow query logs* 
* Review documentation about [slow query logs](https://docs.microsoft.com/azure/mysql/concepts-server-logs) 
* Review how to configure & access logs from the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) and [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli)
* There are two ways slow query logs can be consumed: .log files or Azure diagnostic logging (which routes to storage account, Event Hub, or Azure Monitor logs)


*Audit log*

* 
Learn more about [slow query logs](https://docs.microsoft.com/azure/mysql/concepts-server-logs) and [audit logs](https://docs.microsoft.com/azure/mysql/concepts-audit-logs)
* Review how to configure [slow query logs](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
    * [Audit logs]()
* Verbose logging will cause a significant performance overhead. We recommend you only use statement logging parameters like log_statement and log_min_duration_statement for short periods of troubleshooting. 
* Access to transaction logs is not available

There are two main ways logs can be consumed: .log files or Azure diagnostic logging (which routes to storage account, Event Hub, or Azure Monitor logs).

*.log files*
* .log files provide short-term storage for logs in a CSV-like format. This is the default log option on Azure Database for PostgreSQL.
* The .log files rotate every 1 hour or 100MB size, whichever comes first
* Retention:
  * There is a maximum of 1GB of storage available per server for the .log files. Oldest logs will be deleted to make room for new ones.
  * You can set the retention period for this log storage using the **log_retention_period** parameter. The default value is 3 days; the maximum value is 7 days.
  * You can download logs to store them for longer in your preferred location
  
*Azure Monitor diagnostic logging*

Alternatively, you can use Azure Monitor Diagnostic settings to send logs in JSON format to a storage account, Event Hub, or Azure Monitor logs for longer term storage and analysis.
* Learn how to configure this feature in the Azure Database for PostgreSQL [logs document](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
  * This feature is only available in the General Purpose and Memory Optimized pricing tiers

## **Recommended Documents**
* [Overview on server logs](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
* [Download server logs from the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-logs-in-portal/)<br>
* [Download server logs from the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-logs-using-cli/)



# Logging capabilities in Azure Database for PostgreSQL

## **Recommended Steps**

The Azure Activity Log provides information about subscription-level events. Your Activity Log for Azure Database for PostgreSQL will log ARM-level events like server creation, server scaling, and server delete. Learn more about [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview). 

Database activity auditing is available using the pgAudit extension. 

* pgAudit cannot be used on Basic tier servers. Attempting to set it will cause an error.
* By default, pgAudit log statements are emitted along with your regular log statements by using Postgres's standard logging facility. In Azure Database for PostgreSQL, these .log files can be downloaded through the Azure portal or the CLI.
* Enabling pgAudit generates a large volume of logging on a server, which has an impact on performance and log storage. We recommend that you use the Azure diagnostic log service, which offers longer-term storage options, as well as analysis and alerting features. We recommend that you turn off standard logging to reduce the performance impact of additional logging:

   1. Set the parameter 'logging_collector' to OFF
   2. Restart the server to apply this change

* To install pgAudit, you first need to include it in the server's shared_preload_libraries parameter. This parameter requires a restart to take effect. 
* pgAudit settings are specified globally and cannot be specified at a database or role level
* Setting 'pgaudit.log_client' to ON will redirect logs to a client process (like psql) instead of being written to file. This setting should generally be left disabled.
* 'pgaudit.log_level' is only enabled when 'pgaudit.log_client' is on.
* In Azure Database for PostgreSQL, 'pgaudit.log' cannot be set using a '-' (minus) sign shortcut as described in the pgAudit documentation. All required statement classes (READ, WRITE etc) should be individually specified.
* Use the 'log_line_prefix' parameter to add information like user who executed and database. As an example, the following 'log_line_prefix' setting provides timestamp, username, database name, and process ID: t=%m u=%u db=%d pid=[%p]:

## **Recommended Documents**

* [Auditing in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-audit)
* [Azure Database for PostgreSQL logging](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)



# Auditing capabilities in Azure Database for MySQL

Azure Database for MySQL comes with a rich set of capabilities with regards to auditing capabilities and diagnose the problem. Audit logging is currently in preview.

## **Recommended Steps**

* Review the [Configuring Audit logging on Azure Portal](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-portal) how-to

## **Recommended Documents**

* [Using slow query logs - Portal](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal)<br>
* [Using slow query logs - CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli)
