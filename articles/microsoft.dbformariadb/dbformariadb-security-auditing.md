<properties
    pageTitle="Security in Azure Database for MariaDB"
    description="Security in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="360"
    selfHelpType="generic"
    supportTopicIds="32640112"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5ca7ea17-094e-404e-96ba-46c8ad45aa9c"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Auditing capabilities in Azure Database for MariaDB

Database activity auditing is available using the auditing logging capabilities. Audit logging is currently in preview.

* [Audit logging](https://docs.microsoft.com/azure/mariadb/concepts-audit-logs) is enabled by changing the server parameter **audit_log_enabled** to ON.
* You can select which server events (ex. connection, DML, DDL, etc.) and DB users to log. To view the list of events can be logged, review the [audit logging](https://docs.microsoft.com/azure/mariadb/concepts-audit-logs#configure-audit-logging) concepts document
* It is recommended to only log the event types (using the **audit_log_events** parameter) and users (using the **audit_log_include_users** & **audit_log_exclude_users** parameters) required for your auditing purposes to ensure your server's performance is not heavily impacted.

Audit logs are integrated with Azure Monitor Diagnostic Logs. Once you've enabled audit logs on your MariaDB server, you can emit them to Azure Monitor logs, Event Hubs, or Azure Storage.

## **Recommended Documents**

* [Audit logs](https://docs.microsoft.com/azure/mariadb/concepts-audit-logs)<br>
* [Configure audit logs - Portal](https://docs.microsoft.com/azure/mariadb/howto-configure-audit-logs-portal)<br>
* [Configure audit logs - CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-audit-logs-cli)
