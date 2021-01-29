<properties
    pageTitle="Auditing capabilities in Azure Database for PostgreSQL"
    description="Auditing capabilities in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="450"
    selfHelpType="generic"
    supportTopicIds="32780937"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-security-auditing"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Auditing capabilities in Azure Database for PostgreSQL

## **Recommended Steps**

The Azure Activity Log provides information about subscription-level events. Your Activity Log for Azure Database for PostgreSQL will log ARM-level events such as server creation, server scaling, and server delete. Learn more about the [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview). 

Database activity auditing is available using the `pgAudit` extension:

* `pgAudit` settings are specified globally and cannot be specified at a database or role level
* Setting `pgaudit.log_client` to `ON` will redirect logs to a client process, such as `psql`, instead of being written to file. This setting should generally be left disabled.
* `pgaudit.log_level` is only enabled when `pgaudit.log_client` is on
* In Azure Database for PostgreSQL, `pgaudit.log` cannot be set using a `-` (minus) sign shortcut, as described in the `pgAudit` documentation. All required statement classes (`READ`, `WRITE`, and so on) should be individually specified.
* Use the `log_line_prefix` parameter to add information, such as user who executed and database. As an example, the following `log_line_prefix` setting provides timestamp, username, database name, and process ID: `t=%m u=%u db=%d pid=[%p]:`
* `pgaudit` does not provide connection logging. Connection logging is provided by the Postgres `log_connections` and `log_disconnections` parameters.

## **Recommended Documents**

* [Introduction to `pgaudit`](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/auditing-know-what-s-going-on-in-your-postgres-database/ba-p/885243)
