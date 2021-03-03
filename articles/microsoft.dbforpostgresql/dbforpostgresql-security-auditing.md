<properties
    pageTitle="Auditing capabilities in Azure Database for PostgreSQL"
    description="Auditing capabilities in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="450"
    selfHelpType="generic"
    supportTopicIds="32639967, 32780945"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="2009dc6a-a6bd-41c6-ad36-d7de45e3586f"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Auditing capabilities in Azure Database for PostgreSQL


## **Recommended Steps**

There are two types of activity auditing in Azure Database for PostgreSQL - Single server:
* Azure activity for Azure resource lifecycle events, such as creation, scaling, and others
* Audit of PostgreSQL database activities for sessions and objects

The **Azure Activity Log** provides information about subscription-level events. Your Activity Log for Azure Database for PostgreSQL will log ARM-level events, such as server creation, server scaling, and server delete. Learn more about the [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview). 

**Database activity auditing** is available using the pgAudit extension.

* Are you looking for a database audit option on Basic tier servers?
  `pgAudit` cannot be used on Basic tier servers. Attempting to set it will cause an error.
  
* Are you trying to find out where audit logging is stored?
  By default, `pgAudit` log statements are emitted, along with your regular log statements, by using Postgres's standard logging facility. In Azure Database for PostgreSQL, these `.log` files can be downloaded through the Azure portal (Server logs page) or the CLI.
  
* Do you have a question about URL for `.log` files? 
  The URL generated for accessing your `.log` file is authenticated by using your logged-in user credentials. The URL includes a token that was generated from your authentication. Unauthenticated users can't view the log unless you choose to share the URL.
  
* Are you optimizing logging on your server? Or are you trying to determine how to reduce log size and logging impact on server performance?
  Enabling `pgAudit` generates a large volume of logging on a server, which has an impact on performance and log storage. We recommend that you use the Azure diagnostic log service, which offers longer-term storage options, as well as analysis and alerting features. We also recommend that you turn off standard logging to reduce the performance impact of additional logging, using the following steps:

  1. Set the parameter `logging_collector` to **Off**
  2. Restart the server to apply this change

* Are you looking for the steps to enable `pgAudit` on your server?
  To install `pgAudit`, you first need to include it in the server's `shared_preload_libraries` parameter. This parameter requires a server restart to take effect. 
  
* Are you seeking a way to specify `pgAudit` settings for individual databases and/or roles on your server?
  `pgAudit` settings are specified globally and cannot be specified at a database or role level.
  
* Do you need to redirect logs instead of writing them to a file?
  Setting `pgaudit.log_client` to **On** will redirect logs to a client process (like `psql`) instead of being written to file. This setting should generally be left disabled.
    
* Are you trying to set `pgaudit.log_level` server parameter to a value and not getting expected results?
  Make sure `pgaudit.log_client` is set to **On**. `pgaudit.log_level` is only enabled when `pgaudit.log_client` is on.
  
* Are you using the minus sign ("-") shortcut for `pgaudit.log` parameter?
  In Azure Database for PostgreSQL, `pgaudit.log` can't be set using a minus sign shortcut as described in the `pgAudit` documentation. All required statement classes (`READ`, `WRITE`, and so on) should be individually specified.
  
* Do you need to add a prefix in the beginning of each log line?
  Use the `log_line_prefix` server parameter to add information, such as the user who executed commands and database name. As an example, the following `log_line_prefix` setting provides timestamp, username, database name, and process ID: `t=%m u=%u db=%d pid=[%p]:`
    
* Are you trying to setup connection logging using `pgAudit`?
  `pgAudit` doesn't provide connection logging. Connection logging is provided by Postgres's `log_connections` and `log_disconnections` parameters.

## **Recommended Documents**

* [Introduction to pgaudit](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/auditing-know-what-s-going-on-in-your-postgres-database/ba-p/885243)
* [Auditing in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-audit)
* [Azure Database for PostgreSQL logging](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
* [pgAudit documentation`](https://github.com/pgaudit/pgaudit/blob/master/README.md)
