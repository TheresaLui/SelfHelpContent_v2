<properties
	pageTitle="Diagnose and resolve issues connecting to Azure SQL Database"
	description="Diagnose and resolve issues connecting to Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32630429"
	productPesIds="13491"
	cloudEnvironments="MoonCake"
    resourceTags="servers, databases"
	articleId="sql-availabilityandconnectivity-imeconcounteringanerrorwhenconnecting-new-mooncake"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Diagnose and resolve issues connecting to Azure SQL Database

## **Recommended Documents**

### Error 10928: The session limit for the database is X and has been reached

* The Resource ID indicates which resource governance limit is being hit. A value of 1 is a limit on worker threads; 2 is a limit on sessions (connections). For short term mitigation, increase the [service tier](https://docs.azure.cn/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32630429/) of your database; longer term, tune the workload so it better fits the selected tier. Refer to the [Query Performance Insight](https://docs.azure.cn/sql-database/sql-database-query-performance?WT.mc_id=pid:13491:sid:32630429/) feature for assistance analyzing and tuning your workload.

### Error 18456: Login failed for user X

* Troubleshoot this error using the [Azure SQL Database Connectivity troubleshooter](https://docs.azure.cn/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database#unable-to-log-in-to-the-server-errors-18456-40531?WT.mc_id=pid:13491:sid:32630429/)

### Error 40613: Database X on server Y is not currently available

* This common, transient error occurs when you database is undergoing a reconfiguration, and normally lasts less than 60 seconds. [Read more](https://docs.azure.cn/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database#transient-fault-error-messages-40197-40613-and-others?WT.mc_id=pid:13491:sid:32630429/) about how to handle this. <br>

### Error 40615: Cannot open server X requested by the login

* Resolve this error by creating a server firewall rule as described [here](https://docs.azure.cn/sql-database/sql-database-vnet-service-endpoint-rule-overview#errors-40914-and-40615?WT.mc_id=pid:13491:sid:32630429/)

### Login/connection timeouts

* Ensure your application is using a login timeout of at least 15 seconds. Also confirm that the database is not hitting the [limits](https://docs.azure.cn/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32630429/) of your selected service tier.

### Other error not listed

* [Troubleshoot connectivity issues](https://support.microsoft.com/help/10085/troubleshooting-connectivity-issues-with-microsoft-azure-sql-database?WT.mc_id=pid:13491:sid:32630429/)
* [SQL Database error codes and corrective actions](https://docs.azure.cn/sql-database/sql-database-develop-error-messages?WT.mc_id=pid:13491:sid:32630429/)
