<properties
    pageTitle="Audit logs in Azure Database for MySQL Single Server"
    description="Audit logs in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="andrela"
    ms.author="ajlam"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32747542"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="abe2e640-8e57-48c4-b6a0-37aaa1ef1163"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Audit logs in Azure Database for MySQL Single Server

Azure Database for MySQL Single Server offers audit logs that can be used to track database-level activity including connection, admin, DDL, and DML events. These types of logs are commonly used for compliance purposes.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Enabling audit logs*

Audit logs are disabled by default. Use the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-cli) to enable logs.

*Configuring audit logs*

* Configure events to be logged using the `audit_log_events` server parameter. Refer to [audit log documentation](https://docs.microsoft.com/azure/mysql/concepts-audit-logs) for the full list of events.
* Include or exclude users to be logged using the `audit_log_include_users` and `audit_log_exclude_users` parameters
* It is recommended to only log the event types and users required for your auditing purposes to ensure your server's performance is not heavily impacted

*Accessing audit logs*

* Audit logs are integrated with Azure Monitor diagnostics. This allows your logs (in JSON format) to be emitted to Azure Monitor logs, Event Hubs, or Azure Storage for longer term storage and analysis
* Use your server's **Diagnostic settings** page in the Azure portal to configure where to emit your logs using the "MySqlAuditLogs" log type
* Refer to the [audit logs](https://docs.microsoft.com/azure/mysql/concepts-audit-logs#access-audit-logs) documentation to learn more about log analysis and output

## **Recommended Documents**

* [Audit logs](https://docs.microsoft.com/azure/mysql/concepts-audit-logs)<br>
* [Configure audit logs - Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-portal)<br>
* [Configure audit logs - Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-cli)