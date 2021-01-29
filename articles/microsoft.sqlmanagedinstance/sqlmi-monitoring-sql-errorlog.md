<properties
	pageTitle="SQL errorlog issues with Managed Instance"
	description="SQL errorlog issues with Managed Instance"
	infoBubbleText="SQL errorlog issues with Managed Instance"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748864"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-monitoring-sql-errorlog"
	ownershipId="AzureData_AzureSQLMI"
/>

# **Resolve SQL errorlog issues with Managed Instance**

## **Recommended Steps**

View the SQL Server error log to ensure that processes have completed successfully (for example, backup and restore operations, batch commands, or other scripts and processes). This can be helpful to detect any current or potential problem areas, including automatic recovery messages (particularly if an instance of SQL Server has been stopped and restarted), kernel messages, or other server-level error messages.

### **How to read SQL ErrorLog?**

Use either:
- [Log File Viewer](https://docs.microsoft.com/sql/relational-databases/performance/view-the-sql-server-error-log-sql-server-management-studio?view=sql-server-ver15) in SSMS ([latest SSMS](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15) is strongly recommended)
- sp_readerrorlog stored procedure
- [sp_readmierrorlog](https://github.com/dimitri-furman/managed-instance/tree/master/sp_readmierrorlog) script, more information on the next point

### **There is too much information on the SQL ErrorLog**

* Try the [sp_readmierrorlog](https://github.com/dimitri-furman/managed-instance/tree/master/sp_readmierrorlog) script
* sp_readmierrorlog has the same familiar parameters and result set that sp_readerrorlog has
* It can be created in the master database of each MI instance you use, making it easy to call the procedure from the context of any database on the instance
* The procedure is open source and we would welcome pull requests with changes that make the stored procedure better for all MI customers

### **I've a critical process and I don't want to lose time filtering the SQL errorlog to know what happen**

* Try using the [sp_cycle_errorlog](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-cycle-errorlog-transact-sql?redirectedfrom=MSDN&view=sql-server-ver15) stored procedure before the critical process
* It will close the current error log file and cycles the error log extension numbers just like a server restart. The new error log contains version and copyright information and a line indicating that the new log has been created.

## **Recommended Documents**

* [SQL Server Audit (Database Engine)](https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-database-engine?view=sql-server-ver15)
