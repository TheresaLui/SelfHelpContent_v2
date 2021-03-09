<properties
  pagetitle="Database corruption, recovery, configuration"
  description="database corruption, recovery, configuration"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="ujpat"
  selfhelptype="Resource"
  supporttopicids="32740077"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="04817b04-68fd-46d8-9de9-e9b84373b5c5"
  ownershipid="AzureData_AzureSQLVM" />
# Database corruption, recovery, configuration

4 out of 5 customers are able to resolve their issues with Database corruption, recovery, configuration using the following steps.

## **Recommended Steps**

* **Database Corruption** 
  - To detect database corruption, you can run [DBCC CHECKDB](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-checkdb-transact-sql?view=sql-server-ver15)
  - To resolve and find cause of the corruption or if the database is in suspect mode, follow [Troubleshoot database consistency errors](https://docs.microsoft.com/troubleshoot/sql/admin/troubleshoot-dbcc-errors#resolution)

  - Here are some common corruption errors and their troubleshooting steps 
    [Error 605](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-605-database-engine-error?view=sql-server-ver15), [Error 823](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-823-database-engine-error?view=sql-server-ver15),  [Error 824](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-824-database-engine-error?view=sql-server-ver15),  [Error 825](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-825-database-engine-error?view=sql-server-ver15),  [Error 832](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-832-database-engine-error?view=sql-server-ver15),  [Error 3414](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-3414-database-engine-error?view=sql-server-ver15),  [Error 5180](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-5180-database-engine-error?view=sql-server-ver15), [Error 7105](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-7105-database-engine-error?view=sql-server-ver15), [Error 9004](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-9004-database-engine-error?view=sql-server-ver15), [Error 17204](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-17204-database-engine-error?view=sql-server-ver15),  [Error 17207](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-17207-database-engine-error?view=sql-server-ver15) 


* **Recovery of Databases**

   **If database is recovery pending state, you have to do** 
     - Allow enough time to recovery to complete after SQL instance/database restart  
     - Restore from backup, if there is corruption or previous restore did not complete

  **To avoid database is stuck in recovery pending state, in the future**  

   - For SQL Server 2019 or later, enable [accelerated database recovery](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-and-recovery-overview-sql-server?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support#adr)  
   - Ensure database is corruption free [DBCC CHECKDB](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-checkdb-transact-sql?view=sql-server-ver15)
   - Ensure that transaction log file (*.ldf) [does not have too many VLFs](https://docs.microsoft.com/archive/blogs/saponsqlserver/too-many-virtual-log-files-vlfs-can-cause-slow-database-recovery) 
   - Ensure that [auto_close](https://docs.microsoft.com/sql/relational-databases/policy-based-management/set-the-auto-close-database-option-to-off?view=sql-server-ver15) is turned of 
      
      ```
      ALTER DATABASE [DBName] SET AUTO_CLOSE OFF;
      ```
   - Ensure that tail log backup [does not leave database in restoring mode](https://docs.microsoft.com/sql/relational-databases/backup-restore/back-up-a-transaction-log-sql-server?view=sql-server-ver15#using-sql-server-management-studio).  




## **Recommended Documents**

- Troubleshoot [database consistency errors reported by DBCC CHECKDB](https://support.microsoft.com/help/2015748/how-to-troubleshoot-database-consistency-errors-reported-by-dbcc-check)
- Troubleshoot [database corruption errors](https://techcommunity.microsoft.com/t5/sql-server-support/how-to-troubleshoot-database-corruption-errors-and-system-center/ba-p/316043)
- [Restore and Recovery Overview](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-and-recovery-overview-sql-server?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)