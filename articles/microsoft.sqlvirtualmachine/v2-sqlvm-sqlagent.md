<properties
  pagetitle="SQL Agent or jobs"
  description="SQL agent, jobs, database mail"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740090"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="4622ef61-f0d0-49c6-8c07-b0a40dcd3cac"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Agent or jobs


4 out of 5 customers are able to resolve their issues with SQL Agent or jobs using the following steps.

## **Recommended Steps**


* **If SQL agent service does not start**
  - Ensure that SQL Server Agent service account has [required privileges](https://docs.microsoft.com/sql/ssms/agent/view-sql-server-agent-error-log-sql-server-management-studio?view=sql-server-ver15#to-view-the--agent-error-log) and has access to the required [file and directory](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15#Reviewing_ACLs)
  - Make sure SQL agent service account is a sysadmin in the SQL instance
  - Review the [SQL agent logs](https://docs.microsoft.com/sql/ssms/agent/view-sql-server-agent-error-log-sql-server-management-studio?view=sql-server-ver15#to-view-the--agent-error-log) for possible errors and take corrective action



## **Recommended Documents**

- [SQL Server Agent](https://docs.microsoft.com/sql/ssms/agent/sql-server-agent?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)
- [Select an Account for the SQL Server Agent Service](https://docs.microsoft.com/sql/ssms/agent/select-an-account-for-the-sql-server-agent-service?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)
- [Create a Job](https://docs.microsoft.com/sql/ssms/agent/create-a-job?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)