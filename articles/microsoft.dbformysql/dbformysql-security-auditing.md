<properties
    pageTitle="Auditing capabilities in Azure Database for MySQL"
    description="Auditing capabilities in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32640045"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1086df0a-65e8-428f-8e7d-4ef9b9a19924"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Auditing capabilities in Azure Database for MySQL

The Azure Activity Log provides information about subscription-level events. Your Activity Log for Azure Database for MySQL will log ARM-level events like server creation, server scaling, and server delete. Learn more about [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview).

## **Recommended Steps**

Database activity auditing is available using the auditing logging capabilities. Audit logging is currently in preview.

* [Audit logging](https://docs.microsoft.com/azure/mysql/concepts-audit-logs) is enabled by changing the server parameter **audit_log_enabled** to ON. 
* You can select which server events (ex. connection, DML, DDL, etc.) and DB users to log. To view the list of events can be logged, review the [audit logging](https://docs.microsoft.com/azure/mysql/concepts-audit-logs#configure-audit-logging) concepts document
* It is recommended to only log the event types (using the **audit_log_events** parameter) and users (using the **audit_log_include_users** & **audit_log_exclude_users** parameters) required for your auditing purposes to ensure your server's performance is not heavily impacted.

Audit logs are integrated with Azure Monitor Diagnostic Logs. Once you've enabled audit logs on your MySQL server, you can emit them to Azure Monitor logs, Event Hubs, or Azure Storage.

## **Recommended Documents**

* [Audit logs](https://docs.microsoft.com/azure/mysql/concepts-audit-logs)<br>
* [Configure audit logs - Portal](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-portal)<br>
* [Configure audit logs - CLI](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-cli)
