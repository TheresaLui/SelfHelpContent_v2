<properties
    pageTitle="Audit logs in Azure Database for MySQL"
    description="Audit logs in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="andrela"
    ms.author="ajlam"
    displayOrder="600"
    selfHelpType="generic"
    supportTopicIds="32747996"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b5438323-394a-4ee8-a42b-55622ff9c09c"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Audit logs in Azure Database for MySQL

Azure Database for MySQL Single Server and Flexible Server offer audit logs that can be used to track database-level activity including connection, admin, DDL, and DML events. These types of logs are commonly used for compliance purposes.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Enabling audit logs*

Audit logs are disabled by default. Use the following to enable logs:

* Azure portal: [Single server](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-portal) | [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-configure-audit-logs-portal)
* Azure CLI: [Single server](https://docs.microsoft.com/azure/mysql/howto-configure-audit-logs-cli)

*Configuring audit logs*

* Configure events to be logged using the `audit_log_events` server parameter. Refer to [audit log documentation](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-audit-logs) for the full list of events.
* Include or exclude users to be logged using the `audit_log_include_users` and `audit_log_exclude_users` parameters
* It is recommended to only log the event types and users required for your auditing purposes to ensure your server's performance is not heavily impacted

*Accessing audit logs*

Audit logs are integrated with Azure Monitor diagnostics, which emits logs (in JSON format) to a storage account, Event Hub, or Azure Monitor logs for longer term storage and analysis

## **Recommended Documents**

* [Single server - Audit logs](https://docs.microsoft.com/azure/mysql/concepts-audit-logs)<br>
* [Flexible server - Audit logs](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-audit-logs)