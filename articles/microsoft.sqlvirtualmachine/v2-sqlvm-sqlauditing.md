<properties
  pagetitle="SQL Auditing&#xD;"
  description="SQL Auditing"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740091"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="dfceeaab-3945-4456-b052-6d3673794d49"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Auditing

Most customers are able to resolve issues with SQL Server Auditing by using the following steps. 

## **Recommended Steps** 

- **Error 33204: SQL Server Audit failed to access the security log** 
   
   To resolve, see [this page](https://support.microsoft.com/topic/kb4052136-fix-sql-server-audit-events-fail-to-write-to-the-security-log-d9708450-6981-2fab-4e58-5f09d561110e)
which documents the fix.

- **Error 33208: SQL Server Audit failed to access the security log. Make sure that the SQL service account has the required permissions to access the security log.**    
   
   Make sure to specify the Target to write the Audit events, and that it has the [required permissions to write](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-database-engine?view=sql-server-ver15#target)

- **Set up SQL Server Auditing**

  To enable auditing in SQL Server, you must create the **[Server Audit Specifications](https://docs.microsoft.com/sql/relational-databases/security/auditing/create-a-server-audit-and-server-audit-specification?view=sql-server-ver15)** and **[Database Audit Specifications](https://docs.microsoft.com/sql/relational-databases/security/auditing/create-a-server-audit-and-database-audit-specification?view=sql-server-ver15)**. In "Server Audit", you can set the destination of the audit and the action when it is not available to write to the audit. The Server Audit Specification specifies the server-level actions that you want to audit. Database Audit Specification specifies the database-level action of the action to audit.

- **SQL Threat Detection/Vulnerability Assessments/Azure Defender for SQL Audits Generating errors** 

    To find out the cause, work with Azure Defender Team or disable [Azure Defender Auditing for SQL](https://docs.microsoft.com/azure/azure-sql/database/azure-defender-for-sql#manage-azure-defender-settings) from Security Center.

- **Audit SQL Server Users/Permissions/Password Change** 

   To track these changes, use [Audit Actions and Groups](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions?view=sql-server-ver15)


## **Recommended Documents** 

* [Write SQL Server Audit Events to the Security Log](https://docs.microsoft.com/sql/relational-databases/security/auditing/write-sql-server-audit-events-to-the-security-log?view=sql-server-ver15) 
* [SQL Server Audit](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-database-engine?view=sql-server-ver15)
* [Configure Login Auditing](https://docs.microsoft.com/sql/ssms/configure-login-auditing-sql-server-management-studio?view=sql-server-ver15)
* [Create a server audit and database audit specification](https://docs.microsoft.com/sql/relational-databases/security/auditing/create-a-server-audit-and-database-audit-specification?view=sql-server-ver15)
* [SQL Server Audit Records](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-records?view=sql-server-ver15) 
* [View a SQL Server Audit Log](https://docs.microsoft.com/sql/relational-databases/security/auditing/view-a-sql-server-audit-log?view=sql-server-ver15)
* [Azure Defender for SQL](https://docs.microsoft.com/azure/azure-sql/database/azure-defender-for-sql#manage-azure-defender-settings)
