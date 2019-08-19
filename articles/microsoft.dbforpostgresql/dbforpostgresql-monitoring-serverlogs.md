<properties
    pageTitle="Monitoring server logs"
    description="Monitoring server logs"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="270"
    selfHelpType="generic"
    supportTopicIds="32640020"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="9a898ad6-4234-4b2e-961f-5829895815e7"
/>

# Monitoring Server logs

Azure Database for PostgreSQL generates query and error logs. Query and error logs can be used to identify, troubleshoot, and repair configuration errors and sub-optimal performance.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Review how to [configure server logs](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
* Please note that access to transaction logs is not included.
* The log files rotate every 1 hour or 100MB size, whichever comes first.
* Retention:
  * There is a maximum of 1GB of storage available per server for the .log files. Oldest logs will be deleted to make room for new ones.
  * You can set the retention period for this log storage using the **log_retention_period** parameter. The default value is 3 days; the maximum value is 7 days
  * You can download logs to store them for longer in your preferred location. Alternatively, you use Azure Monitor Diagnostic settings to send them to a storage account, event hub, or Azure Monitor logs. Learn more in the Azure Database for PostgreSQL [logs document](https://docs.microsoft.com/azure/postgresql/concepts-server-logs).
  * The Azure Monitor Logs feature is only available in the General Purpose and Memory Optimized pricing tiers

## **Recommended Documents**

* [Download server logs from the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-logs-in-portal/)<br>
* [Download server logs from the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-logs-using-cli/)
