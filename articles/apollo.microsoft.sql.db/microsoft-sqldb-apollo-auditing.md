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
        •	Retain an audit trail of selected events. You can define categories of database actions to be audited.
        •	Report on database activity. You can use pre-configured reports and a dashboard to get started quickly with activity and event reporting.
        •	Analyze reports. You can find suspicious events, unusual activity, and trends.
## Setup and Configuration:
    To Enable Auditing at server and database level, below are the available options:
        •	Demo: Setup and Configuration of Auditing Step-by-Step using Portal or CLI
        •	Please see the recommended video and documentation links to setup and configure Azure SQL auditing.
### Recommended video
            In the following video, you will learn about the setup and configuration for Auditing your Azure SQL database.
<video>
<src>https://www.youtube.com/watch?v=7uDloadggmA&feature=youtu.be</src>
<title>Demo: Setup and Configuration of Auditing in Azure SQL</title>
</video>
    
    Below is the information discussed in Demo:
        •	Go to [Azure Portal](https://portal.azure.com/) and Navigate to Auditing under the Security heading in your SQL database or SQL server pane
        •	Create or Update auditing for Azure SQL server and database using [Azure PowerShell](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#using-azure-powershell)
        •	Create or Update auditing for Azure SQL server and database using [REST API](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#using-rest-api)
            o	If you are using Storage account, one of the key requirement is to generate [Storage key generation](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#storage-key-regeneration)
            o	Auditing Geo-replication databases, please follow the [recommendations](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#auditing-geo-replicated-databases)
        •	Get [Auditing policy](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#manage-auditing) status once its enabled on a Server or database using 
        •	Remove or [Disable Auditing](https://docs.microsoft.com/en-us/azure/azure-sql/database/auditing-overview#manage-auditing)

## Troubleshooting:
        •	Write audit to a storage account behind VNet and Firewall
        •	With Azure Storage, the audit logs can be made immutable. Follow these instructions, making sure you have selected Allow additional appends.
        •	Auditing on Read-Only Replicas is automatically enabled. For further details about the hierarchy of the storage folders, naming conventions, and log format, go to SQL Database Audit Log Format.
        •	For auditing of successful and failed logins, note the following:
            o	Logins are routed by the gateway to the specific instance where the database is located.
            o	In the case of AAD logins, the credentials are verified before attempting to use that user to login into the requested database. In the case of failure, the requested database is never accessed, so no auditing occurs. To view failed logins, you need to visit the Azure Active Directory portal, which logs details of these events.
            o	In the case of SQL logins, the credentials are verified on the requested data, so failed logins can be audited.
            o	Successful logins, which obviously reach the database, are audited in both cases.
        •	Monitoring, Logging and Auditing in Azure SQL DB is shown in below video for step-by step information on
            o	Server level Audit
            o	Database level Audit
            o	What is monitored and managed using Auditing and how to view the logs based on the Auditing
### Recommended video: Understanding Azure SQL auditing and monitoring concepts 
        In the following video, you will learn about the strategies and methods for monitoring and auditing your Azure SQL database.

<video>
<src>https://www.youtube.com/watch?v=HeKDc-ndlYc</src>
<title>Monitoring, Logging, and Auditing in Azure SQL</title>
</video>

        This video will highlight the following auditing capabilities:

        Audit Azure level activities with Azure Monitor Logs
        Use Activity Logs and RBAC auditing for Azure Monitoring
        Setup alerts for Advanced Threat Protection
        Monitor Azure Security Center

## Additional Information for Auditing:

Once Auditing is configured, below are the recommendations to monitor, generate reports

    •	Permissions and Access for Auditing
    o	Permission required: Azure built-in roles - Azure RBAC | Microsoft Docs
    o	Auditing:
               Edit audit settings :  
                Microsoft.Sql/servers/auditingSettings/*
                Microsoft.Sql/servers/databases/auditingSettings/* or Microsoft.Sql/servers/extendedAuditingSettings/*
    o	Retrieve audit records in the portal : Microsoft.Sql/servers/databases/auditRecords/read
    o	Additional permissions for storage account behind VNet:
            On the storage account: Microsoft.Authorization/roleAssignments/write 
    o	Additional permissions for auditing to Azur Monitor: 
            	Microsoft.Insights/DiagnosticSettings/*
    •	Audit Events 
        o	An Audition policy can be defined for a specific database or as a default server policy in Azure which hosts ( SQL Database or Synapse). Please review more details at Server-Level Auditing vs. Database-Level Auditing
        o	Audit Actions and Action Groups
            	Default policy includes (not applicable to Managed Instance):
•	BATCH_COMPLETED_GROUP
•	SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP
•	FAILED_DATABASE_AUTHENTICATION_GROUP
o	Location of Audit Logs for integration 
	Azure Storage
•	Audit logs stored in Azure blob storage are stored in a container named sqldbauditlogs in Azure Storage
	Audit events are written to Log Analytics workspace defined during auditing configuration, to the AzureDiagnostics table with the category SQLSecurityAuditEvents. For additional useful information about Log Analytics search language and commands, see Log Analytics search reference.
•	Log Analytics (preview, GA estimated for March 2021)
	Audit events are written to the namespace and event hub that was defined during auditing configuration, and are captured in the body of Apache Avro events and stored using JSON formatting with UTF-8 encoding. To read the audit logs, you can use Avro Tools or similar tools that process this format.
•	Event Hub (preview, GA estimated for March 2021)
	Audit Log Retention settings are managed at storage integration configured, by default most of the retention periods are 0(Unlimited retention). You can change this value as per the requirement for compliance.
	Audit log fields and format are available for reference.
•	Using the Audit Logs
o	Use the Azure portal. Open the relevant database. At the top of the database's Auditing page, select View audit logs
o	If you are planning to use TSQL please follow the document Consuming audit logs though TSQL
•	More Tutorials and workshop:
o	Playlist: Azure SQL for Beginners
o	View Code on GitHub
o	Live Bootcamp

## Limitations:
Below are the current product limitations
•	Premium storage is currently not supported.
•	Hierarchical namespace for Azure Data Lake Storage Gen2 storage account is currently not supported.
•	Enabling auditing on a paused Azure Synapse is currently not supported. To enable auditing, resume Azure Synapse.
•	Email notifications are sent to the subscription admins/co-admins and subscription owner.  These are currently not configurable.

## Auditing Upcoming Preview Features:
    o	Auditing of Microsoft Support Operations (Preview, GA estimated for first half of 2021)
        	For more information about this Preview feature in Azure SQL Database and Azure Synapse Analytics, go to these instructions.
        	For Managed Instance, create an audit using the following T-SQL:
        •	CREATE SERVER AUDIT [MyAudit] TO EXTERNAL_MONITOR WITH (OPERATOR_AUDIT = ON)

## Feedback:
    Do you have an idea or suggestion based on your experience with Azure? We would love to hear it! Please take a few minutes to submit your idea in the one of the forums available on the right or vote up an idea submitted by another Azure customer. All of the feedback you share in these forums will be monitored and reviewed by the Microsoft engineering teams responsible for building Azure.

•	SQL Database: Customer Feedback for ACE Community Tooling





