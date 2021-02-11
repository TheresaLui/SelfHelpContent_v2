<properties
    pageTitle="Monitoring server logs"
    description="Monitoring server logs"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="270"
    selfHelpType="generic"
    supportTopicIds="32640020, 32780887"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9a898ad6-4234-4b2e-961f-5829895815e7"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Monitoring server logs

Azure Database for PostgreSQL has error, query, and audit logs available. Use query and error logs to identify, troubleshoot, and repair configuration errors and sub-optimal performance. Go to **Security** > **Auditing** for troubleshooting guidance on audit logs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Review how to [configure server logs](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
* Familiarize yourself with the [log parameters](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/how-to-configure-postgres-log-settings/ba-p/1214716)
* Verbose logging will cause a significant performance overhead. We recommend you only use statement logging parameters like `log_statement` and `log_min_duration_statement` for short periods of troubleshooting. 
* Access to transaction logs is not available

There are two main ways logs can be consumed: as .log files, or through Azure diagnostic logging (which routes to storage account, Event Hub, or Azure Monitor logs).

### .log files

* .log files provide short-term storage for logs in a CSV-like format. This is the default log option on Azure Database for PostgreSQL.
* The .log files rotate every hour or when it reaches 100 MB in size, whichever comes first
* Retention:
  * The maximum storage for .log files, per server, is 1 GB. Oldest logs are deleted to make room for new logs.
  * Set the retention period for log storage using the **log_retention_period** parameter. The default value is 3 days; the maximum value is 7 days.
  * To bypass this limit, download logs using standard CLI/Portal and store them in your preferred location. If you encounter timeouts because of slower network speeds, download the files using [Microsoft Download Manager](https://www.microsoft.com/en-us/p/download-manager/9wzdncrfj2rp?activetab=pivot:overviewtab). 
  * The URL generated for accessing your .log file is authenticated using your logged-in user credentials. The URL includes a token that is generated during authentication. Unauthenticated users cannot view the log unless you choose to share the URL.
  
### Azure Monitor diagnostic logging

Alternatively, you can use Azure Monitor Diagnostic settings to send logs in JSON format to a storage account, Event Hub, or Azure Monitor logs for longer term storage and analysis.

* Learn how to configure this feature in the Azure Database for PostgreSQL [logs document](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)

	* This feature is only available in the General Purpose and Memory Optimized pricing tiers

## **Recommended Documents**

* [Overview on server logs](https://docs.microsoft.com/azure/postgresql/concepts-server-logs)
* [Download server logs from the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-logs-in-portal/)<br>
* [Download server logs from the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-logs-using-cli/)
