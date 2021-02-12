<properties
  pagetitle="Back up a managed instance database to Azure Blob Storage"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="katmac"
  selfhelptype="Generic"
  supporttopicids="32637314"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="b951b1c5-2d93-4c5a-8fc6-836421bda563"
  ownershipid="AzureData_AzureSQLMI" />
# Back up a managed instance database to Azure Blob Storage

In addition to [automatically managed backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database), Azure SQL Managed Instance enables you to manually make COPY_ONLY backups of a database to Azure Blob Storage using the Transact-SQL BACKUP TO URL statement.

## **Recommended Steps**

- Verify that you are using [supported syntax in your statement](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#restore-statement)
- For detail on SQL Managed Instance backup limitations, see [T-SQL Differences between SQL Server and Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/transact-sql-tsql-differences-sql-server#backup)

**Message 33111: Cannot Find Server Certificate with Thumbprint**

- Determine if the backup is protected with Transparent Data Encryption (TDE). If it is, [disable the TDE protection](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Take-a-backup-of-TDE-protected-database-on-Azure-SQL-Managed/ba-p/643407#M120) in order to run a manual backup.

**Message 3063: Write to Backup Blob Device…failed. Device has reached its limit of allowed blocks**

- Add the following options to the Backup statement: MAXTRANSFERSIZE=4194304, BLOCKSIZE=65536, and COMPRESS

**Message 3202: Write on … failed: 1117 (The request could not be performed because of an I/O device error.)**
- Add the following options to the Backup statement: MAXTRANSFERSIZE=4194304, BLOCKSIZE=65536, and COMPRESS

**Unable to Create a Manual Backup**
- Use a [credential in an SAS Token](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/tutorial-linux-vm-access-storage-sas). Note that:

  * The CREDENTIAL NAME argument requires that the name match the container path, start with https, and not contain a trailing forward slash
  * The IDENTITY argument requires the name and, SHARED ACCESS SIGNATURE
  * The SECRET argument requires the shared access signature token
  * The SHARED ACCESS SIGNATURE secret should not have the leading question mark (?)
  * Check whether the SECRET option of the CREATE CREDENTIAL statement is valid within your SAS credential. The most common errors within the SAS token are: incorrect expiration date (se), start date (st), and permission property (sp).

## **Recommended Documents**

- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)
- [Take a backup of TDE protected database on Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Take-a-backup-of-TDE-protected-database-on-Azure-SQL-Managed/ba-p/643407#M120)
- [Automate migration to Managed Instance using PowerShell](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Automate-migration-to-Managed-Instance-using-PowerShell/ba-p/830801#M186)
