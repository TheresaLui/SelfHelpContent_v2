<properties
    pageTitle="Auditing capabilities in Azure Database for PostgreSQL"
    description="Auditing capabilities in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="450"
    selfHelpType="generic"
    supportTopicIds="32639967"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2009dc6a-a6bd-41c6-ad36-d7de45e3586f"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Auditing capabilities in Azure Database for PostgreSQL

## **Recommended Steps**

The Azure Activity Log provides information about subscription-level events. Your Activity Log for Azure Database for PostgreSQL will log ARM-level events like server creation, server scaling, and server delete. Learn more about [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview). 

Database activity auditing is available using the pgAudit extension:

* pgAudit cannot be used on Basic tier servers. Attempting to set it will cause an error.
* By default, pgAudit log statements are emitted along with your regular log statements by using Postgres's standard logging facility. In Azure Database for PostgreSQL, these .log files can be downloaded through the Azure portal or the CLI.
* The URL generated for accessing your .log file is authenticated using your logged in user's credentials. The URL includes a token that was generated from your authentication. Unauthenticated users cannot view the log unless you choose to share the URL.
* Enabling pgAudit generates a large volume of logging on a server, which has an impact on performance and log storage. We recommend that you use the Azure diagnostic log service, which offers longer-term storage options, as well as analysis and alerting features. We recommend that you turn off standard logging to reduce the performance impact of additional logging:

   1. Set the parameter 'logging_collector' to OFF
   2. Restart the server to apply this change

* To install pgAudit, you first need to include it in the server's shared_preload_libraries parameter. This parameter requires a restart to take effect. 
* pgAudit settings are specified globally and cannot be specified at a database or role level
* Setting 'pgaudit.log_client' to ON will redirect logs to a client process (like psql) instead of being written to file. This setting should generally be left disabled.
* 'pgaudit.log_level' is only enabled when 'pgaudit.log_client' is on
* In Azure Database for PostgreSQL, 'pgaudit.log' cannot be set using a '-' (minus) sign shortcut as described in the pgAudit documentation. All required statement classes (READ, WRITE etc) should be individually specified.
* Use the 'log_line_prefix' parameter to add information like user who executed and database. As an example, the following 'log_line_prefix' setting provides timestamp, username, database name, and process ID: `t=%m u=%u db=%d pid=[%p]:`
* pgaudit does not provide connection logging. This is provided by Postgres's log_connections and log_disconnections parameters.

## **Recommended Documents**

* [Introduction to pgaudit](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/auditing-know-what-s-going-on-in-your-postgres-database/ba-p/885243)
* [Auditing in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-audit)
* [Azure Database for PostgreSQL logging](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
