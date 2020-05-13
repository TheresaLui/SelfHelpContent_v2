<properties
	pageTitle="Managed Instance - Log size misconfiguration"
	description="Managed Instance - Log size misconfiguration"
	infoBubbleText="Managed Instance space used for log files is insufficient. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="v-zlrade"
	authors="v-zlrade"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_Log size misconfiguration"
	selfHelpType="diagnostics"
	supportTopicIds="32637300,32637306,32637313"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-perf-log-size-misconfiguration"
	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Log size misconfiguration

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> was facing insufficient space for log files between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime-->.

When the transaction log becomes full, SQL Server Database Engine issues a 9002 error. If the log fills while the database is online, the database remains online but can only be read, not updated. 

<!--/issueDescription-->

## **Recommended Steps**

* To enable normal operation of your instance, you will need to increase the space reserved for log files on your storage for the following affected databases:

  <!--$affectedDatabases-->affectedDatabases<!--/$affectedDatabases-->

* If you have free, unneeded space on your instance, you can [enlarge your log files](<https://docs.microsoft.com/sql/relational-databases/logs/manage-the-size-of-the-transaction-log-file?view=sql-server-2017#AddOrEnlarge>). To enlarge the log file, use the __MODIFY FILE__ clause of the __ALTER DATABASE__ statement, specifying the __SIZE__ syntax, as described in the following example:

  ```sql
  alter database database_name
         modify file (name='file_name', size = 300GB)
  ```

* Otherwise, if you don't have enough free storage on your instance, consider updating your SLO and getting more storage. To update your SLO you should:

  1. Navigate to the Managed Instance in Azure Portal
  2. Select *"Pricing Tier"* 
  3. Increase storage size 
  4. Click *"Apply"* 

## **Recommended Documents**

* [ALTER DATABASE (Transact-SQL) File and Filegroup options](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-file-and-filegroup-options?view=sql-server-2017)
* [Managing the size of the transactional log file](https://docs.microsoft.com/sql/relational-databases/logs/manage-the-size-of-the-transaction-log-file?view=sql-server-2017#AddOrEnlarge)

