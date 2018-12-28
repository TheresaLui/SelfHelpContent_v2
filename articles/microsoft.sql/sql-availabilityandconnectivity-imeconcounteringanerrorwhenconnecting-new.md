<properties
	pageTitle="availability and connectivity/I'm encountering an error when connecting to my database"
	description="availability and connectivity/I'm encountering an error when connecting to my database"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    authorAlias="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630429"
	productPesIds="13491"
	cloudEnvironments="public"
/>

# availability and connectivity/I'm encountering an error when connecting to my database

## **Recommended documents**

### Error 10928: The session limit for the database is X and has been reached

* The Resource ID indicates which resource governance limit is being hit.  A value of 1 is a limit on worker threads; 2 is a limit on sessions (connections).  For short term mitigation, increase the [service tier](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu) of your database; longer term, tune the workload so it better fits the selected tier. Refer to the [Query Performance Insight](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance) feature for assistance analyzing and tuning your workload. <br>

### Error 18456: Login failed for user X

* Troubleshoot this error using the [Azure SQL Database troubleshooter](https://support.microsoft.com/help/10085/troubleshooting-connectivity-issues-with-microsoft-azure-sql-database) <br>

### Error 40613: Database X on server Y is not currently available

* This common, transient error occurs when you database is undergoing a reconfiguration, and normally lasts less than 60 seconds. [Read more](https://docs.microsoft.com/azure/sql-database/sql-database-troubleshoot-common-connection-issues) about how to handle this. <br>

### Error 40615: Cannot open server X requested by the login

* Resolve this error by creating a server firewall rule as described [here](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview#errors-40914-and-40615) <br>

### Login/connection timeouts

* Ensure your application is using a login timeout of at least 15 seconds.  Also confirm that the database is not hitting the [limits](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu) of your selected service tier.

### Other error not listed

* [Troubleshoot connectivity issues](https://support.microsoft.com/help/10085/troubleshooting-connectivity-issues-with-microsoft-azure-sql-database)<br>
* [SQL Database error codes and corrective actions](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages)<br>
* [Steps to fix common connection issues](https://docs.microsoft.com/azure/sql-database/sql-database-troubleshoot-common-connection-issues#try-the-troubleshooter-for-azure-sql-database-connectivity-issues)