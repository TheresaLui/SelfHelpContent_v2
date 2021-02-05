<properties
pageTitle="Auditing"
description="Azure SQL DB Auditing"
ms.author="sojaga,dabrookl"
displayOrder=""
articleId="801225fa-6137-492e-bc10-74bf3b1327a0"
selfHelpType="Apollo"
supportTopicIds="3d771302-d96b-2fe9-9e72-6ff138fd1d05"
productPesIds="13491"
cloudEnvironments="public"
ownershipId="AzureData_AzureSQLDB_Security"
/>

# Auditing and Monitoring

## Auditing Overview:

Auditing writes database events to an audit log. Auditing helps you maintain regulatory compliance, understand database activity, and gain insight into discrepancies and anomalies that could indicate business concerns or suspected security violations.

-   Retain an audit trail of selected events. You can define categories of database actions to be audited.
-   Report on database activity. You can use pre-configured reports and a dashboard to get started quickly with activity and event reporting.
-   Analyze reports. You can find suspicious events, unusual activity, and trends.

## Setup and Configuration:

To enable auditing at the server and database level, you have the available options:

-   Demo: Setup and Configuration of Auditing Step-by-Step using Portal or CLI


### Recommended video
In the following video, you will learn how to configure Azure SQL Auditing step-by-step. 

<video>
      <src>https://www.youtube.com/watch?v=7uDloadggmA&feature=youtu.be</src>
      <title>Demo: Configure Auditing for Azure SQL Database</title>
</video>  


### Summary of configuration steps in the video:

1.   Go to [Azure Portal](https://portal.azure.com/) and navigate to **Auditing** under the Security heading in your SQL database or SQL server pane. (Demo video is below.)
1.   Create or Update auditing for Azure SQL server and database, using one of the following methods:
      - [Azure PowerShell](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#using-azure-powershell)
      - [REST API](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#using-rest-api)

1.   If you're using a Storage account, one of the key requirement is to generate [Storage key generation](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#storage-key-regeneration)

1.   To audit Geo-replication databases, see these [recommendations](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#auditing-geo-replicated-databases)

1. After auditing is enabled, use the following links to:
   -   Get status on [Auditing policy](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#manage-auditing)  
   -   Remove or [Disable Auditing](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#manage-auditing)

## Troubleshooting:

-   Write audit to a storage account behind [VNet and Firewall](https://docs.microsoft.com/en-us/azure/azure-sql/database/audit-write-storage-account-behind-vnet-firewall)
-   With Azure Storage, the audit logs can be made immutable. Follow these [instructions](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fstorage%2Fblobs%2Fstorage-blob-immutability-policies-manage%23enabling-allow-protected-append-blobs-writes&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271968668%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=gs3YR6mSq5Piyk%2FzhoV96YpmIRwudgpEUv26El4ocD4%3D&reserved=0), making sure you have selected Allow additional appends.
-   Auditing on [Read-Only Replicas](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-sql%2Fdatabase%2Fread-scale-out&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271978664%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=UlkvQFxCZ%2BiH8IkVV%2B5rit2HZR359D4jHatp7coAf9o%3D&reserved=0) is automatically enabled. For further details about the hierarchy of the storage folders, naming conventions, and log format, go to [SQL Database Audit Log Format](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-sql%2Fdatabase%2Faudit-log-format&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271978664%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=79nmf1KQdvPhVe3X1QujBS9u7I%2BRoey4BwmjNQBd2%2F0%3D&reserved=0).
-   For auditing of successful and failed logins, note the following:

    -   Logins are routed by the gateway to the specific instance where the database is located.
    -   In the case of AAD logins, the credentials are verified before attempting to use that user to login into the requested database. In the case of failure, the requested database is never accessed, so no auditing occurs. To view failed logins, you need to visit the [Azure Active Directory portal](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Factive-directory%2Freports-monitoring%2Freference-sign-ins-error-codes&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271988658%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=G6T4p%2B7sOoJgvcePbbnKJz%2FcaZiRi5BE469F0yJdyLw%3D&reserved=0), which logs details of these events.
    -   In the case of SQL logins, the credentials are verified on the requested data, so failed logins can be audited.
    -   Successful logins, which obviously reach the database, are audited in both cases.

-   Monitoring, Logging and Auditing in Azure SQL DB is shown in below video for step-by step information on

    -   Server level Audit
    -   Database level Audit
    -   What is monitored and managed using Auditing and how to view the logs based on the Auditing

### Recommended video
In the following video, you will learn about monitoring, logging and auditing of Azure SQL. 

<video>
<src>https://www.youtube.com/watch?v=HeKDc-ndlYc&feature=youtu.be</src>
<title>Monitoring, Logging and Auditing for Azure SQL Database</title>
</video>  

### Additional Information for Auditing:

After Auditing is configured, follow these recommendations to monitor, generate reports:

-   [Permissions and Access for Auditing](https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/create-a-server-audit-and-server-audit-specification?view=sql-server-ver15#Permissions)

    -   Permission required: [Azure built-in roles - Azure RBAC | Microsoft Docs](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Frole-based-access-control%2Fbuilt-in-roles&data=04%7C01%7Csojaga%40microsoft.com%7C3cfbba7e873b488d56ee08d8c3da18ce%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637474688789312048%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=af1kDPVR8MKwCVur5rCLTuTkDNitNdyvP1eXuq%2B46g0%3D&reserved=0)
    -   Auditing:

    -   Edit audit settings :

          [Microsoft.Sql](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Frole-based-access-control%2Fresource-provider-operations%23microsoftsql&data=04%7C01%7Csojaga%40microsoft.com%7C3cfbba7e873b488d56ee08d8c3da18ce%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637474688789321992%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=iPnb8DqBmu%2Fr%2FkeOei4vymfoLKUvRq0HI7t3www7YHk%3D&reserved=0)/servers/auditingSettings/*

          [Microsoft.Sql](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Frole-based-access-control%2Fresource-provider-operations%23microsoftsql&data=04%7C01%7Csojaga%40microsoft.com%7C3cfbba7e873b488d56ee08d8c3da18ce%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637474688789331966%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=SYcvZe0iQauYwqgZEmth858yZLp%2B1ARZ%2BClCCLDrefY%3D&reserved=0)/servers/databases/auditingSettings/* or M[icrosoft.Sql](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Frole-based-access-control%2Fresource-provider-operations%23microsoftsql&data=04%7C01%7Csojaga%40microsoft.com%7C3cfbba7e873b488d56ee08d8c3da18ce%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637474688789331966%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=SYcvZe0iQauYwqgZEmth858yZLp%2B1ARZ%2BClCCLDrefY%3D&reserved=0)/servers/extendedAuditingSettings/*

    -   Retrieve audit records in the portal : [Microsoft.Sql](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Frole-based-access-control%2Fresource-provider-operations%23microsoftsql&data=04%7C01%7Csojaga%40microsoft.com%7C3cfbba7e873b488d56ee08d8c3da18ce%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637474688789351869%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=F68Z0tbeKFdM4A4gCRt9mcaDqOmSaMm5%2FOutkLcZ6jE%3D&reserved=0)/servers/databases/auditRecords/read
    -   Additional permissions for storage account behind VNet:

        On the storage account: `Microsoft.Authorization/roleAssignments/write`

    -   Additional permissions for auditing to Azur Monitor:

        -   [Microsoft.Insights](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Frole-based-access-control%2Fresource-provider-operations%23microsoftinsights&data=04%7C01%7Csojaga%40microsoft.com%7C3cfbba7e873b488d56ee08d8c3da18ce%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637474688789351869%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=1pOWFzkd3BmPy6A%2FTNrMW2JQ1OLKL8qOK%2BXQTDGOuVU%3D&reserved=0)
        /DiagnosticSettings/*

-   Audit Events

    -   An Audition policy can be defined for a specific database or as a default server policy in Azure which hosts ( SQL Database or Synapse). Please review more details at [Server-Level Auditing vs. Database-Level Auditing](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-sql%2Fdatabase%2Fauditing-overview%23server-vs-database-level&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271838726%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=fldIWUm42EY9vgthDyerfKHCE99CwlMLWX5f5VsEvsE%3D&reserved=0)
    -   [Audit Actions and Action Groups](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fsql%2Frelational-databases%2Fsecurity%2Fauditing%2Fsql-server-audit-action-groups-and-actions%3Fview%3Dsql-server-ver15&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271848722%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=fe5UpLZ2j184xl%2BiBbigKdF4khmigjGjxSdTv8b7SOE%3D&reserved=0)

        -   Default policy includes (not applicable to Managed Instance):

            -   BATCH_COMPLETED_GROUP
            -   SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP
            -   FAILED_DATABASE_AUTHENTICATION_GROUP

-   Location of Audit Logs for integration

    -   [Azure Storage](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#audit-storage-destination)

        -   Audit logs stored in Azure [blob storage](https://docs.microsoft.com/en-us/azure/azure-sql/database/audit-log-format#blob-audit) are stored in a container named _sqldbauditlogs_ in Azure Storage

        -   Audit events are written to Log Analytics workspace defined during auditing configuration, to the `_AzureDiagnostics_` table with the category `_SQLSecurityAuditEvents_`. For additional useful information about Log Analytics search language and commands, see [Log Analytics search reference](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/log-query-overview).

    -   [Log Analytics](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#audit-log-analytics-destination) (preview, GA estimated for March 2021)

        -   Audit events are written to the namespace and event hub that was defined during auditing configuration, and are captured in the body of [Apache Avro](https://avro.apache.org/) events and stored using JSON formatting with UTF-8 encoding. To read the audit logs, you can use [Avro Tools](https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-capture-overview#use-avro-tools) or similar tools that process this format.

    -   [Event Hub](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#audit-event-hub-destination) (preview, GA estimated for March 2021)

        -   Audit Log Retention settings are managed at storage integration configured, by default most of the retention periods are 0(Unlimited retention). You can change this value as per the requirement for compliance.
        -   Audit log fields and format are available for [reference](https://docs.microsoft.com/en-us/azure/azure-sql/database/audit-log-format#subheading-1).

-   Using the Audit Logs

    -   Use the [Azure portal](https://portal.azure.com/). Open the relevant database. At the top of the database's **Auditing** page, select **[View audit logs](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#subheading-3)**
    -   If you are planning to use TSQL please follow the document [Consuming audit logs though TSQL](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fsql%2Frelational-databases%2Fsystem-functions%2Fsys-fn-get-audit-file-transact-sql%3Fview%3Dsql-server-ver15&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271948674%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=10YRLOdqHVgsG1KiH0Y37JR7ycJp5p4Sy9dVHit4ODE%3D&reserved=0)

-   More Tutorials and workshop:

    -   Playlist: [Azure SQL for Beginners](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fwww.youtube.com%2Fplaylist%3Flist%3DPLlrxD0HtieHi5c9-i_Dnxw9vxBY-TqaeN&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271998654%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=zA2kCwL477hNMvE12xNpX0GYUfAXEzehZ41DSauLgQg%3D&reserved=0)
    -   [View Code on GitHub](https://www.youtube.com/redirect?v=HeKDc-ndlYc&redir_token=QUFFLUhqbmMwN3JXTDhwZkdBa2dLelJpbGt0XzNuMUppQXxBQ3Jtc0tsZ2JUb0xteTBMVldLQ0NXN21uMU9RVEk0SnkyM0ZEbnN0d1cxb09VQzEwajJ2T25HSkRTR2Z0dDJrNnhzMkFseWpJOHJfb1pjRmRYcERmd0NUY1dRVGhZXy1wY04zbHVVM1Y5Y2kxUkxPY3NhcUVUYw%3D%3D&q=https%3A%2F%2Faka.ms%2Fasqlworkshop&event=video_description)
    -   [Live Bootcamp](https://www.youtube.com/redirect?v=HeKDc-ndlYc&redir_token=QUFFLUhqbERKbk9JdG5IeVR4Vi1qbVhaTU1ld29OY0NHUXxBQ3Jtc0tud1VVeVp5eEVzLVRCb0NnSGRzc0o2djM5bndYeXJjUG85YURmWjg5YnVDVDBiTDgzNU9qT1ZIY3dKS21vYVJWY0M2QW5QZm1nbUgwdTl3RU9UUjN5alZRUjhSUlQtb3QyQ1hPa2tVVjV3Z0ZnMXFuQQ%3D%3D&q=https%3A%2F%2Faka.ms%2Fazuresqlbootcamp&event=video_description)

## Limitations:

Below are the current product limitations

-   Premium storage is currently not supported.
-   Hierarchical namespace for Azure Data Lake Storage Gen2 storage account is currently not supported.
-   Enabling auditing on a paused Azure Synapse is currently not supported. To enable auditing, resume Azure Synapse.
-   Email notifications are sent to the subscription admins/co-admins and subscription owner. These are currently not configurable.

## Auditing Upcoming Preview Features:

-   Auditing of Microsoft Support Operations (Preview, GA estimated for first half of 2021)

    -   For more information about this Preview feature in Azure SQL Database and Azure Synapse Analytics, go to these [instructions](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-sql%2Fdatabase%2Fauditing-overview%23auditing-of-microsoft-support-operations&data=04%7C01%7Ckatmac%40microsoft.com%7C276adb231edb439f9b6d08d8bdb22de3%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637467920271858715%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=eOKuIrjd4gF%2F91g%2F14sF96Na%2BITZ0TieloMEZHDufEg%3D&reserved=0).
    -   For Managed Instance, create an audit using the following T-SQL:

    -   CREATE SERVER AUDIT [MyAudit] TO EXTERNAL_MONITOR WITH (OPERATOR_AUDIT = ON)
