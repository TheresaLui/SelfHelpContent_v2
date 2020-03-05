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
    cloudEnvironments="public, Fairfax"
    articleId="1086df0a-65e8-428f-8e7d-4ef9b9a19924"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Auditing capabilities in Azure Database for MySQL

The Azure Activity Log provides information about subscription-level events. Your Activity Log for Azure Database for MySQL will log ARM-level events like server creation, server scaling, and server delete. Learn more about [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview). 

## **Recommended Steps**

Database activity auditing is available using the auditing logging capabilities. Audit logging is currently in preview.

* Audit logging is enabled by changing the server parameter **audit_log_enabled** to ON. 
* You can select the events to log (ex. connection, DML, DDL, etc.). To understand what events can be logged, review the [Configuring Audit logging on Azure Portal](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-portal) how-to document

Audit logs are integrated with Azure Monitor Diagnostic Logs. Once you've enabled audit logs on your MySQL server, you can emit them to Azure Monitor logs, Event Hubs, or Azure Storage.

## **Recommended Documents**

* [Using slow query logs - Portal](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal)<br>
* [Using slow query logs - CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli)
