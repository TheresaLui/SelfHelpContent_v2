<properties
  pagetitle="Azure SQL DB Security Auditing"
  description="Azure SQL Database Security Auditing"
  ms.author="sojaga,dabrookl"
  selfhelptype="Apollo"
  supporttopicids="3d771302-d96b-2fe9-9e72-6ff138fd1d05"
  resourcetags=""
  productpesids="13491"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="fe0e2955-03fb-4b82-95f9-c57153de3786"
  ownershipid="AzureData_AzureSQLDB_Security" />

# Auditing

## Overview, setup, and configuration of SQL Database Auditing 

This article guides users through setup and configuration of Azure SQL DB Auditing. Included is a configuration demo video, and a list of known issues and limitations.

:::Section Configuration demo:::

## Demo: How to Configure Auditing for Azure SQL Database

View the following demo of configuring Auditing Azure SQL Database and documentation to address common questions during setup and configuration.

<video>
    <src>https://www.youtube.com/watch?v=7uDloadggmA</src>
    <title>Demo: Configure Auditing for Azure SQL Database</title>
</video>


:::Section Overview of SQL DB Auditing:::

## What does SQL DB Auditing do?:

Azure SQL Database Auditing writes database events to an audit log. Auditing helps you maintain regulatory compliance, understand database activity, and gain insight into discrepancies and anomalies that could indicate business concerns or suspected security violations.

This feature enables and facilitates adherence to compliance standards, although it doesn't guarantee compliance. For more information about Azure programs that support standards compliance, see the [Azure Trust Center](https://www.microsoft.com/en-us/trust-center/?rtc=1) where you can find the most current list of Azure SQL compliance certifications.

Here are some benefits of the Auditing feature:
 - Retain an audit trail of selected events. You can define categories of database actions to be audited.
 - Report on database activity. You can use pre-configured reports and a dashboard to get started quickly with activity and event reporting.
 - Analyze reports. You can find suspicious events, unusual activity, and trends.


:::Section Configuration and setup:::

## **Configure and set up Auditing**

 1. Go to [Azure Portal](https://portal.azure.com/). Under the Security heading in your SQL database or SQL server pane, go to **Auditing**. (See also the Demo video is the previous section.)
2. Create or update Auditing for Azure SQL Server and Database, using one of the following methods: [Azure PowerShell](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#using-azure-powershell), [REST API](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#using-rest-api).
3. If you're using a Storage account, one of the key requirement is to generate [Storage key generation](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#storage-key-regeneration)
4. To audit Geo-replication databases, see these [recommendations](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#auditing-geo-replicated-databases)
5. After auditing is enabled, use the following links to Get status on [Auditing policy](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#manage-auditing)
6. Remove or [Disable Auditing](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#manage-auditing)


:::Section Considerations and known issues:::

## Review these issues with Auditing settings and workflow:

 1. Write audit to a storage account behind [VNet and Firewall](https://docs.microsoft.com/azure/azure-sql/database/audit-write-storage-account-behind-vnet-firewall)
 2. With Azure Storage, the audit logs can be made immutable. Follow these [instructions](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutability-policies-manage?tabs=azure-portal), making sure you have selected Allow additional appends.
 3. Auditing on [Read-Only Replicas](https://docs.microsoft.com/azure/azure-sql/database/read-scale-out) is automatically enabled. For further details about the hierarchy of the storage folders, naming conventions, and log format, go to [SQL Database Audit Log Format](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format).
 4. For Auditing successful and failed logins, note the following:
	 * Logins are routed by the gateway to the specific instance where the database is located.
	 * In the case of AAD logins, the credentials are verified before attempting to use that user to login into the requested database. In the case of failure, the requested database is never accessed, so no auditing occurs. To view failed logins, you need to visit the [Azure Active Directory portal](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-sign-ins-error-codes), which logs details of these events.
	* In the case of SQL logins, the credentials are verified on the requested data, so failed logins can be audited.
	* Successful logins, which obviously reach the database, are audited in both cases.


:::Section Permissions and access:::

### Required Permissions and access for Azure SQL DB Auditing setup and view logs:

[Permissions and Access for Auditing](https://docs.microsoft.com/sql/relational-databases/security/auditing/create-a-server-audit-and-server-audit-specification?view=sql-server-ver15#Permissions)
 - Permission required: [Azure built-in roles - Azure RBAC | Microsoft Docs](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
 - Edit Auditing settings :
	- [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/auditingSettings/*
	- [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/databases/auditingSettings/* or 
	- [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/extendedAuditingSettings/*
 - Retrieve audit records in the portal: [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftsql)/servers/databases/auditRecords/read
 - Additional permissions for storage account behind VNet:
	 - On the storage account: `Microsoft.Authorization/roleAssignments/write`
- Additional permissions for Auditing to Azure Monitor:
	- [Microsoft.Insights](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftinsights)/DiagnosticSettings/*
- Audit Events
	- An Audition policy can be defined for a specific database or as a default server policy in Azure which hosts ( SQL Database or Synapse). Please review more details at [Server-Level Auditing vs. Database-Level Auditing](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#server-vs-database-level)
	-	[Audit Actions and Action Groups](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions?view=sql-server-ver15)
- Default policy includes (not applicable to Managed Instance):
	- `BATCH_COMPLETED_GROUP`
	- `SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP`
	- `FAILED_DATABASE_AUTHENTICATION_GROUP`
 

:::Section Log integration and storage:::

### Azure SQL DB Auditing logs integration and storage:

- Location of Audit Logs for integration
	-  [Azure Storage](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-storage-destination)
		- Audit logs stored in Azure [blob storage](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format#blob-audit) are stored in a container named _sqldbauditlogs_ in Azure Storage
  -  [Log Analytics](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-log-analytics-destination) 
		- Audit events are written to Log Analytics workspace defined during auditing configuration, to the `_AzureDiagnostics_` table with the category `_SQLSecurityAuditEvents_`. For additional useful information about Log Analytics search language and commands, see [Log Analytics search reference](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview).
	-  [Event Hub](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-event-hub-destination)
		- Audit events are written to the namespace and event hub that was defined during auditing configuration, and are captured in the body of [Apache Avro](https://avro.apache.org/) events and stored using JSON formatting with UTF-8 encoding. To read the audit logs, you can use [Avro Tools](https://docs.microsoft.com/azure/event-hubs/event-hubs-capture-overview#use-avro-tools) or similar tools that process this format.
- Audit Log Retention settings are managed at storage integration configured, by default most of the retention periods are 0(Unlimited retention). You can change this value as per the requirement for compliance.
- Audit log fields and format are available for [reference](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format#subheading-1).
- View Auditing Logs
	- Use the [Azure portal](https://portal.azure.com/). Open the relevant database. At the top of the database's **Auditing** page, select [View audit logs](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#subheading-3)
	- If you are planning to use TSQL please follow the document [Consuming audit logs though TSQL](https://docs.microsoft.com/sql/relational-databases/system-functions/sys-fn-get-audit-file-transact-sql?view=sql-server-ver15)
	- For Managed Instance, create an audit using the following T-SQL:
	- CREATE SERVER AUDIT [MyAudit] TO EXTERNAL_MONITOR WITH (OPERATOR_AUDIT = ON)


:::Section Limitations:::

## Review these current Auditing limitations

 - Premium storage is currently not supported. 
 - Hierarchical namespace for Azure Data Lake Storage Gen2 storage account is currently not supported. 
 - Enabling auditing on a paused Azure Synapse is currently
   not supported. 
	 - To enable auditing, resume Azure Synapse. 
 - Email notifications are sent to the subscription admins/co-admins and
   subscription owner. 
   * These are currently not configurable. 


  :::Section Upcoming features:::

## Azure SQL DB Auditing features in preview:

 - Auditing of Microsoft Support Operations (Preview, GA estimated for first half of 2021)
 - For more information about this Preview feature in Azure SQL Database and Azure Synapse Analytics, go to these [instructions](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#auditing-of-microsoft-support-operations).

:::Section More resources:::

### See the following recommended Documents and demo videos

- Playlist: [Azure SQL for Beginners](https://www.youtube.com/watch?v=Dtr6eRVZQ8I&list=PLlrxD0HtieHi5c9-i_Dnxw9vxBY-TqaeN) This video series covers the challenges, solutions, and key benefits to Azure SQL. For the full [Azure SQL Fundamentals](https://docs.microsoft.com/learn/paths/azure-sql-fundamentals/?WT.mc_id=azuresql4beg_azuresql-ch9-ninert) learning path on Microsoft Learn and  [View Code on GitHub](https://microsoft.github.io/sqlworkshops/?WT.mc_id=azuresql4beg_azuresql-ch9-code)
- [Auditing Public Documentation](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview)
- [What's new in Azure SQL Auditing](https://www.youtube.com/watch?v=QXDpVzAJ4qA)
