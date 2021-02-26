<properties
	pageTitle="security, privacy and compliance/auditing"
	description="security, privacy and compliance/auditing"
	service="microsoft.sql"
	resource="servers"
	authors="sojaga"
   	ms.author="sojaga"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630407"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="9fcb9dab-5912-42b6-b6d8-9d0a4bd18c87"
	ownershipId="AzureData_AzureSQLDB_Security"
/>

# Auditing and Monitoring

## Auditing Overview:

Auditing writes database events to an audit log. Auditing helps you maintain regulatory compliance, understand database activity, and gain insight into discrepancies and anomalies that could indicate business concerns or suspected security violations.

-   Retain an audit trail of selected events. You can define categories of database actions to be audited.
-   Report on database activity. You can use pre-configured reports and a dashboard to get started quickly with activity and event reporting.
-   Analyze reports. You can find suspicious events, unusual activity, and trends.

## **Recommended Steps for Setup and Configuration:**

1.   Go to [Azure Portal](https://portal.azure.com/) and navigate to Auditing under the Security heading in your SQL database or SQL server pane. (Demo video is below.)
1.   Create or Update auditing for Azure SQL server and database, using one of the following methods:
      - [Azure PowerShell](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#using-azure-powershell)
      - [REST API](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#using-rest-api)

1.   If you're using a Storage account, one of the key requirement is to generate [Storage key generation](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#storage-key-regeneration)

1.   To audit Geo-replication databases, see these [recommendations](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#auditing-geo-replicated-databases)

1. After auditing is enabled, use the following links to:
   -   Get status on [Auditing policy](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#manage-auditing)  
   -   Remove or [Disable Auditing](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#manage-auditing)

## Troubleshooting:

-   Write audit to a storage account behind [VNet and Firewall](https://docs.microsoft.com/azure/azure-sql/database/audit-write-storage-account-behind-vnet-firewall)
-   With Azure Storage, the audit logs can be made immutable. Follow these [instructions](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutability-policies-manage?tabs=azure-portal), making sure you have selected Allow additional appends.
-   Auditing on [Read-Only Replicas](https://docs.microsoft.com/azure/azure-sql/database/read-scale-out) is automatically enabled. For further details about the hierarchy of the storage folders, naming conventions, and log format, go to [SQL Database Audit Log Format](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format).
-   For auditing of successful and failed logins, note the following:

    -   Logins are routed by the gateway to the specific instance where the database is located.
    -   In the case of AAD logins, the credentials are verified before attempting to use that user to login into the requested database. In the case of failure, the requested database is never accessed, so no auditing occurs. To view failed logins, you need to visit the [Azure Active Directory portal](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-sign-ins-error-codes), which logs details of these events.
    -   In the case of SQL logins, the credentials are verified on the requested data, so failed logins can be audited.
    -   Successful logins, which obviously reach the database, are audited in both cases.

-   Monitoring, Logging and Auditing in Azure SQL DB is shown in below video for step-by step information on

    -   Server level Audit
    -   Database level Audit
    -   What is monitored and managed using Auditing and how to view the logs based on the Auditing

### Additional Information for Auditing:

After Auditing is configured, follow these recommendations to monitor, generate reports:

-   [Permissions and Access for Auditing](https://docs.microsoft.com/sql/relational-databases/security/auditing/create-a-server-audit-and-server-audit-specification?view=sql-server-ver15#Permissions)

    -   Permission required: [Azure built-in roles - Azure RBAC | Microsoft Docs](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
    -   Auditing:

    -   Edit audit settings :

          [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/auditingSettings/*

          [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/databases/auditingSettings/* or M[icrosoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/extendedAuditingSettings/*

    -   Retrieve audit records in the portal : [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/databases/auditRecords/read
    -   Additional permissions for storage account behind VNet:

        On the storage account: `Microsoft.Authorization/roleAssignments/write`

    -   Additional permissions for Auditing to Azure Monitor:

        -   [Microsoft.Insights](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftinsights)
        /DiagnosticSettings/*

-   Audit Events

    -   An Audition policy can be defined for a specific database or as a default server policy in Azure which hosts ( SQL Database or Synapse). Please review more details at [Server-Level Auditing vs. Database-Level Auditing](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#server-vs-database-level)
    -   [Audit Actions and Action Groups](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions?view=sql-server-ver15)

        -   Default policy includes (not applicable to Managed Instance):

            -   BATCH_COMPLETED_GROUP
            -   SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP
            -   FAILED_DATABASE_AUTHENTICATION_GROUP

-   Location of Audit Logs for integration

    -   [Azure Storage](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-storage-destination)

        -   Audit logs stored in Azure [blob storage](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format#blob-audit) are stored in a container named _sqldbauditlogs_ in Azure Storage

        -   Audit events are written to Log Analytics workspace defined during auditing configuration, to the `_AzureDiagnostics_` table with the category `_SQLSecurityAuditEvents_`. For additional useful information about Log Analytics search language and commands, see [Log Analytics search reference](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview).

    -   [Log Analytics](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-log-analytics-destination) (preview, GA estimated for March 2021)

        -   Audit events are written to the namespace and event hub that was defined during auditing configuration, and are captured in the body of [Apache Avro](https://avro.apache.org/) events and stored using JSON formatting with UTF-8 encoding. To read the audit logs, you can use [Avro Tools](https://docs.microsoft.com/azure/event-hubs/event-hubs-capture-overview#use-avro-tools) or similar tools that process this format.

    -   [Event Hub](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-event-hub-destination) (preview, GA estimated for March 2021)

        -   Audit Log Retention settings are managed at storage integration configured, by default most of the retention periods are 0(Unlimited retention). You can change this value as per the requirement for compliance.
        -   Audit log fields and format are available for [reference](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format#subheading-1).

-   Using the Audit Logs

    -   Use the [Azure portal](https://portal.azure.com/). Open the relevant database. At the top of the database's **Auditing** page, select [View audit logs](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#subheading-3)
    -   If you are planning to use TSQL please follow the document [Consuming audit logs though TSQL](https://docs.microsoft.com/sql/relational-databases/system-functions/sys-fn-get-audit-file-transact-sql?view=sql-server-ver15)
    -   For Managed Instance, create an audit using the following T-SQL:
        -   CREATE SERVER AUDIT [MyAudit] TO EXTERNAL_MONITOR WITH (OPERATOR_AUDIT = ON)

-   More Tutorials and workshop:

    -   Playlist: [Azure SQL for Beginners](https://www.youtube.com/watch?v=Dtr6eRVZQ8I&list=PLlrxD0HtieHi5c9-i_Dnxw9vxBY-TqaeN) This video series covers the challenges, solutions, and key benefits to Azure SQL.  For the full Azure SQL Fundamentals learning path on Microsoft Learn, [Azure SQL Fundamentals](https://docs.microsoft.com/learn/paths/azure-sql-fundamentals/?WT.mc_id=azuresql4beg_azuresql-ch9-ninert)    
    -   Select workshop based on your requirement and [View Code on GitHub](https://microsoft.github.io/sqlworkshops/?WT.mc_id=azuresql4beg_azuresql-ch9-code​)
    -   Learn live from Azure SQL DB [Live Bootcamp](https://www.youtube.com/playlist?list=PLlrxD0HtieHjveswk8_gkPD42Te48X4zG&WT.mc_id=learnlive-video-learn)

## Limitations:

Below are the current product limitations

-   Premium storage is currently not supported.
-   Hierarchical namespace for Azure Data Lake Storage Gen2 storage account is currently not supported.
-   Enabling auditing on a paused Azure Synapse is currently not supported. To enable auditing, resume Azure Synapse.
-   Email notifications are sent to the subscription admins/co-admins and subscription owner. These are currently not configurable.

## Auditing Upcoming Preview Features:

-   Auditing of Microsoft Support Operations (Preview, GA estimated for first half of 2021)

    -   For more information about this Preview feature in Azure SQL Database and Azure Synapse Analytics, go to these [instructions](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#auditing-of-microsoft-support-operations).

