<properties
	pageTitle="Distributed Transactions issues with Managed Instance"
	description="Distributed Transactions issues with Managed Instance"
	infoBubbleText="Distributed Transactions issues with Managed Instance"
	service="microsoft.sql"
	resource="managedinstances"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32749585"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-dist-transactions.md"
	ownershipId="AzureData_AzureSQLMI"
/>

# Resolve Distributed Transactions issues with Managed Instance

Distributed transactions can be executed across different Azure SQL Managed Instances using distributed transactions. This feature is currently in **preview mode**.

##Recommended steps

If you are experiencing some issues with distributed transactions, the following steps can help you find a way to troubleshoot the issues.

- In case of error MSDTC not available, go through connectivity and security steps below
- In scenarios with multiple instances check connectivity between them
  - In case distributed transaction with linked server is failing, try to execute a simple select query on the linked server. This query might indicate if the problem is with the linked server setup rather than distributed transactions. Basic requirement for linked servers is that ports 1433, 11000 - 12000 are allowed
  - If instances are part of the same Subnet, there are no additional requirements on the Subnet level and instances are expected to use custom port from range 11000-12000
  - If instances are not part the same subnet, port 5024 needs to be open on all subnets for all participating instances and also, port range 11000-12000 needs to be open on all subnets for all participating instances
  - If instances are on different VNets check if VNet peering is setup properly
- Check if security requirements are satisfied
  - Verify that instances are added to the Server Trust Group
- To resolve stuck, deadlocked, orphaned or in-doubt distributed transactions use kill unit of work (or session id). For more details, please use [KILL documentation](https://docs.microsoft.com/sql/t-sql/language-elements/kill-transact-sql?view=sql-server-ver15)

## **Recommended Documents**
- [Distributed transactions across cloud databases (preview)](https://docs.microsoft.com/azure/azure-sql/database/elastic-transactions-overview)
- [T-SQL differences between SQL Server & Azure SQL Managed Instance (Distributed transactions)](https://docs.microsoft.com/azure/azure-sql/managed-instance/transact-sql-tsql-differences-sql-server#distributed-transactions)
