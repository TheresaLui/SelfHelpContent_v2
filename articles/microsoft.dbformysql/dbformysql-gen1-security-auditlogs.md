<properties
    pageTitle="Auditing capabilities in Azure Database for MySQL Single Server"
    description="Auditing capabilities in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32747543"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="df700559-2bad-490c-a7b1-70a93cfdcf03"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Auditing capabilities in Azure Database for MySQL Single Server

The Azure Activity Log provides information about subscription-level events. Your Activity Log for Azure Database for MySQL will log ARM-level events like server creation, server scaling, and server delete. Learn more about [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview).

Audit logs are also available and can be used to track database-level activity including connection, admin, DDL, and DML events. These types of logs are commonly used for compliance purposes.

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