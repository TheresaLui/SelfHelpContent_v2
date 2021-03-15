<properties
  pagetitle="Azure SQL DB Security Auditing"
  description="Azure SQL Database Security Auditing"
  ms.author="sojaga"
  selfhelptype="apollo"
  supporttopicids="3d771302-d96b-2fe9-9e72-6ff138fd1d05"
  resourcetags=""
  productpesids="13491"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="fe0e2955-03fb-4b82-95f9-c57153de3786"
  ownershipid="AzureData_AzureSQLDB_Security"
  resourcerequired="False" />
# SQL Auditing

## SQL Database Auditing

This article covers everything you need to know about SQL Database Auditing. You’ll learn about how Auditing works, its benefits, and how to configure it

:::Section Configuration demo:::

## Demo: How to Configure Auditing for Azure SQL Database

View the following demo of configuring Auditing Azure SQL Database and documentation to address common questions during setup and configuration.

<video>
<src>https://www.youtube.com/watch?v=7uDloadggmA</src>
<title>Demo: Configure Auditing for Azure SQL Database</title>
</video>
<br><br>

:::Section What is SQL DB Auditing?:::

## Overview

SQL Auditing writes database events to an audit log. Auditing helps you maintain regulatory compliance, understand database activity, and gain insight into discrepancies and anomalies that could indicate business concerns or suspected security violations.

SQL Auditing enables and facilitates adherence to compliance standards, although it doesn't guarantee compliance. For more information about Azure programs that support standards compliance, see the [Azure Trust Center]([Microsoft Trust Center Home](https://www.microsoft.com/trust-center/?rtc=1)) where you can find the most current list of Azure SQL compliance certifications.

Here are some benefits of the Auditing feature:

 - Retain an audit trail of selected events. You can define categories of database actions to be audited.
 - Report on database activity. You can use pre-configured reports and a dashboard to get started quickly with activity and event reporting.
 - Analyze reports. You can find suspicious events, unusual activity, and trends.

*Deciding what to audit*

 - An auditing policy can be defined as a default server policy (recommended) or for a specific database.  Please see [Server-Level Auditing vs. Database-Level Auditing]([Azure SQL Auditing for Azure SQL Database and Azure Synapse Analytics - Azure SQL Database | Microsoft Docs](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview?WT.mc_id=Portal-Microsoft_Azure_Support#server-vs-database-level)) for more details.
 - The choice of which events to audit is configured through [Audit Actions and Action Groups]([SQL Server Audit Action Groups and Actions - SQL Server | Microsoft Docs](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)).
	 - Default policy includes (not applicable to Managed Instance):
		 - BATCH_COMPLETED_GROUP
		 - SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP
		 - FAILED_DATABASE_AUTHENTICATION_GROUP

*Location of Audit Logs*

 - [Azure Storage](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-storage-destination)
	-   Audit logs stored in Azure [blob storage](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format?WT.mc_id=Portal-Microsoft_Azure_Support#blob-audit) are stored in a container named _sqldbauditlogs_ in Azure Storage
 - [Log Analytics](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-log-analytics-destination)
	-   Audit events are written to Log Analytics workspace defined during auditing configuration, to the `**_AzureDiagnostics_**` table with the category `**_SQLSecurityAuditEvents_**`. For additional useful information about Log Analytics search language and commands, see [Log Analytics search reference](https://docs.microsoft.com/azure/azure-monitor/logs/log-query-overview?WT.mc_id=Portal-Microsoft_Azure_Support).

 - [Event Hub](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#audit-event-hub-destination)
	-   Audit events are written to the namespace and event hub that was defined during auditing configuration, and are captured in the body of [Apache Avro](https://avro.apache.org/) events and stored using JSON formatting with UTF-8 encoding. To read the audit logs, you can use [Avro Tools](https://docs.microsoft.com/azure/event-hubs/event-hubs-capture-overview?WT.mc_id=Portal-Microsoft_Azure_Support#use-avro-tools) or similar tools that process this format.

 Audit Log Retention settings are managed at storage integration configured, by default most of the retention periods are 0(Unlimited retention). You can change this value as per the requirement for compliance.
  
:::Section Steps to Setup and configure Auditing:::

## **Setup and configuration**

 1.  SQL Auditing can be setup from the [Azure Portal](https://portal.azure.com/). Under the Security heading in your SQL database or SQL server pane, go to **Auditing**. (See also the Demo video is the previous section.)
 2. Alternatively, SQL Auditing can be configured programmatically using one of the following methods:
	* [Azure PowerShell](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#using-azure-powershell), 
	* [REST API](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview#using-rest-api).
	* [Azure CLI](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview?WT.mc_id=Portal-Microsoft_Azure_Support#using-azure-cli)
	* [ARM Templates](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview?WT.mc_id=Portal-Microsoft_Azure_Support#using-azure-resource-manager-templates)

:::Section Considerations and known issues:::

## Common Solutions and Limitations:

 - **Common Issues and Solutions**
	 - When auditing to a storage account behind a VNet and firewall, follow these [instructions](https://docs.microsoft.com/azure/azure-sql/database/audit-write-storage-account-behind-vnet-firewall?WT.mc_id=Portal-Microsoft_Azure_Support).
	 - With Azure Storage, the audit logs can be made immutable by following these [instructions](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutability-policies-manage?tabs=azure-portal&WT.mc_id=Portal-Microsoft_Azure_Support)
	 - Auditing on [Read-Only Replicas](https://docs.microsoft.com/azure/azure-sql/database/read-scale-out?WT.mc_id=Portal-Microsoft_Azure_Support) is automatically enabled.  For further details about the hierarchy of the storage folders, naming conventions, and log format, go to [SQL Database Audit Log Format](https://docs.microsoft.com/azure/azure-sql/database/audit-log-format?WT.mc_id=Portal-Microsoft_Azure_Support).
	 - For Auditing successful and failed logins, note the following:
		 - Logins are routed by the gateway to the specific instance where the database is located.
		 - In the case of AAD logins, the credentials are verified before attempting to use that user to login into the requested database. In the case of failure, the requested database is never accessed, so no auditing occurs. To view failed logins, you need to visit the [Azure Active Directory portal](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-sign-ins-error-codes?WT.mc_id=Portal-Microsoft_Azure_Support), which logs details of these events.
		 - In the case of SQL logins, the credentials are verified on the requested data, so failed logins can be audited.
		 - Successful logins, which obviously reach the database, are audited in both cases.

 - **Limitations**
	 - Premium storage is currently not supported.
	 - Hierarchical namespace for Azure Data Lake Storage Gen2 storage account is currently not supported.
	 - Enabling auditing on a paused Azure Synapse is currently not supported.
		 - To enable auditing, resume Azure Synapse.
	 - Email notifications are sent to the subscription admins/co-admins and subscription owner.
		 - These are currently not configurable.

:::Section Permissions and access:::

### Required Permissions and access:

 - [SQL Permissions for Auditing](https://docs.microsoft.com/sql/relational-databases/security/auditing/create-a-server-audit-and-server-audit-specification?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support#Permissions)
 - [Azure built-in roles - Azure RBAC](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles?WT.mc_id=Portal-Microsoft_Azure_Support)
 - Edit Auditing settings
	 - [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations?WT.mc_id=Portal-Microsoft_Azure_Support#microsoftsql)/servers/auditingSettings/*
	 - [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations?WT.mc_id=Portal-Microsoft_Azure_Support#microsoftsql)/servers/databases/auditingSettings/*
	 - [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations?WT.mc_id=Portal-Microsoft_Azure_Support#microsoftsql)/servers/extendedAuditingSettings/*
 - Retrieve audit records in the portal:
	 - [Microsoft.SQL](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations?WT.mc_id=Portal-Microsoft_Azure_Support#microsoftsql)/servers/databases/auditRecords/read
 - Additional permissions for storage account behind VNet:
	 - On the storage account: Microsoft.Authorization/roleAssignments/write
 - Additional permissions for Auditing to Azure Monitor:
	 - [Microsoft.Insights](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations?WT.mc_id=Portal-Microsoft_Azure_Support#microsoftinsights)/DiagnosticSettings/*  

:::Section Log integration and storage:::

### Viewing Audit Logs:

 - Use the [Azure portal](https://portal.azure.com/#home).  Open the relevant database.  At the top of the database's Auditing page, select [View audit logs](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview?WT.mc_id=Portal-Microsoft_Azure_Support#subheading-3).
 - If you are planning to use TSQL please follow the document [Consuming audit logs though TSQL](https://docs.microsoft.com/sql/relational-databases/system-functions/sys-fn-get-audit-file-transact-sql?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support).
 - For Managed Instance, create an audit using the following T-SQL:
	 - CREATE SERVER AUDIT [MyAudit] TO EXTERNAL_MONITOR WITH (OPERATOR_AUDIT = ON)[SQL Permissions for Auditing](https://docs.microsoft.com/sql/relational-databases/security/auditing/create-a-server-audit-and-server-audit-specification?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support#Permissions).

:::Section More resources:::

### Additional Resources:
- Playlist: [Azure SQL for Beginners](https://www.youtube.com/watch?v=Dtr6eRVZQ8I&list=PLlrxD0HtieHi5c9-i_Dnxw9vxBY-TqaeN) 
	- This video series covers the challenges, solutions, and key benefits to Azure SQL. 
	- For the full [Azure SQL Fundamentals](https://docs.microsoft.com/learn/paths/azure-sql-fundamentals/?WT.mc_id=azuresql4beg_azuresql-ch9-ninert) learning path on Microsoft Learn and [View Code on GitHub](https://microsoft.github.io/sqlworkshops/?WT.mc_id=azuresql4beg_azuresql-ch9-code)
-  [Auditing Public Documentation](https://docs.microsoft.com/azure/azure-sql/database/auditing-overview)
-  [What's new in Azure SQL Auditing](https://www.youtube.com/watch?v=QXDpVzAJ4qA)