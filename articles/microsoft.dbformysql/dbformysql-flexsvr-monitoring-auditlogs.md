<properties
    pageTitle="Audit logs in Azure Database for MySQL Flexible Server"
    description="Audit logs in Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="andrela"
    ms.author="ajlam"
    displayOrder="190"
    selfHelpType="generic"
    supportTopicIds="32747596"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="cb5f228e-1b3b-4424-aabd-a3daa2436871"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Audit logs in Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible Server offers audit logs that can be used to track database-level activity including connection, admin, DDL, and DML events. These types of logs are commonly used for compliance purposes.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Enabling audit logs*

Audit logs are disabled by default. Use the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-configure-audit-logs-portal) or Azure CLI to enable logs.

*Configuring audit logs*

* Configure events to be logged using the `audit_log_events` server parameter. Refer to [audit log documentation](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-audit-logs) for the full list of events.
* Include or exclude users to be logged using the `audit_log_include_users` and `audit_log_exclude_users` parameters
* It is recommended to only log the event types and users required for your auditing purposes to ensure your server's performance is not heavily impacted

*Accessing audit logs*

* Audit logs are integrated with Azure Monitor diagnostics. This allows your logs (in JSON format) to be emitted to Azure Monitor logs, Event Hubs, or Azure Storage for longer term storage and analysis
* Use your server's **Diagnostic settings** page in the Azure portal to configure where to emit your logs using the "MySqlAuditLogs" log type
* Refer to the [audit logs](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-audit-logs#access-audit-logs) documentation to learn more about log analysis and output

## **Recommended Documents**

* [Audit logs](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-audit-logs)<br>
* [Configure audit logs - Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-configure-audit-logs-portal)