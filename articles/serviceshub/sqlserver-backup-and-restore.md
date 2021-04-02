<properties
 pageTitle="Database Backup or Restore"
 description="Database Backup or Restore"
 articleId="adb1c915-6300-4a62-a2fc-617f6f23bb3e"
 productFamilyId = "7aa8b5ba-4d1a-644d-aeca-bc4decdb15de"
 productPesIds="16907,16899,16893,16887,16881"
 supportTopicIds="32684306"
 ms.author="ramakoni"
 ownershipId="serviceshub"
 selfHelpType="generic"
 cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
/>

# Database Backup or Restore

## **Recommended Steps**

Most users are able to resolve their backup and restore issues with SQL Server using the following steps and documents. Please scroll down for detailed troubleshooting information about each error.

### Summary

This troubleshooter helps you the following backup/restore issues

- Backups taking a long time
- Issues restoring database between different SQL versions
- Issues with backup tasks in Always On environments
- Errors when restoring a database from backup
- Scheduled backups via maintenance plan or SQL Agent jobs are not working
- Backup or restore operations that use third-party backup applications are failing
- Issues restoring encrypted databases
- Issues with compressed backups

It also provides general troubleshooting tips that can help solve backup/restore issues with SQL server.

### Backups taking a long time

Backup and restore operations are I/O intensive. Backup/Restore throughput depends on how well the underlying I/O subsystem is optimized to handle the I/O volume. If you suspect that the backup operations are either hung or taking a long time to complete, you can use one or more of the following methods to estimate the time for completion or to track the progress of backup and restore operations:

- Check SQL Server errorlog for information about past backup and restore operations
- Use [backup_restore_progress_trace](https://docs.microsoft.com/sql/relational-databases/backup-restore/back-up-and-restore-of-sql-server-databases?view=sql-server-ver15#monitor-progress-with-xevent) xEvent to monitor the progress.
- Use the percent_complete column of sys.dm_exec_requests to track the progress of in-flight backup and restore operations.
- Use Device throughput Bytes/sec and Backup/Restore throughput/sec performance monitor counters to measure throughput information.
- Check Activity monitor to see if the backup threads are blocked by other statements and take steps to resolve the blocking situation.
- Use the script found [here](https://github.com/microsoft/mssql-support/blob/master/sample-scripts/backup_restore/estimate_backup_restore.sql) to get an estimate on backup times.

### Issues restoring databases between different SQL versions

No SQL Server backup can be restored to an earlier version of SQL Server than the version on which the backup was created. You can use the procedure below to create a copy of database that is hosted on a later version of SQL Server on an earlier version of SQL Server.  
Note: The following procedure assumes you have two SQL Server instances named SQL_A (higher version) and SQL_B (lower version).

1. Download and install the latest version of [SQL Server Management Studio (SSMS](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15)) on both SQL_A and SQL_B.

1. On SQL_A, take the following steps:

   1. Right click your database>Tasks>Generate Scripts, and select the option to script entire database and all database objects.
   1. Select Advanced on the Set Scripting Options screen and select the version of SQL_B under General>Script for SQL Server Version. Also select the option that works best for you to save the generated scripts and continue with the rest of the steps in the wizard.
   1. Use [bcp](https://docs.microsoft.com/sql/tools/bcp-utility?view=sql-server-ver15#examples) to copy out data from different tables.

1. On SQL_B take the following steps
   1. Use the scripts you generated on SQL_A to create database schema.
   1. On each of the tables, disable any foreign key constraints, triggers and if the table has any identity columns, enable identity insert.
   1. Use bcp to import the data that you exported in previous step into corresponding tables.
   1. After the data import is complete, enable foreign key constraints, triggers and disable identity insert for each of the tables that are affected in step 3(b).

This procedure typically works well for smaller to medium size databases. For larger databases you can run into memory issues in SSMS and other tools and you should consider using SSIS, Replication or other options to create a copy of a database from a higher version on a lower version of SQL server.  
For more information on generating scripts for your database review [Script a database by using the Generate Scripts option](https://docs.microsoft.com/sql/ssms/tutorials/scripting-ssms?view=sql-server-ver15#script-a-database-by-using-the-generate-scripts-option)

### Issues with backup tasks in Always On environments

If you are running into issues with backup jobs or maintenance plans in Always On environments, please note the following:

1. By default, automated backup preference is set to Prefer Secondary which specifies that backups should occur on a secondary replica except when the primary replica is the only replica online. You cannot take differential backups of your database with this setting. To change this setting use SSMS on your current primary replica and navigate to Backup Preferences page under Properties of your Availability group.

1. If you are using maintenance plan or scheduled jobs to generate backups of your databases, be sure to create the job(s) for each availability database on every server instance that hosts an availability replica for the availability group.

For more information regarding backup in Always On environments review the following topics:

1. [Configure backups on secondary replicas of an Always On availability group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-backup-on-availability-replicas-sql-server?view=sql-server-ver15)
1. [Offload supported backups to secondary replicas of an availability group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/active-secondaries-backup-on-secondary-replicas-always-on-availability-groups?view=sql-server-ver15)

### Errors when restoring a database from backup

If you are receiving errors indicating that there is an issue with the file, it is a symptom of a corrupt backup file. You can use [Restore Header](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-headeronly-transact-sql?view=sql-server-ver15) statement to check your backups. Examples of errors you may experience when a backup set is corrupt include, but not limited to the following:

- 3241:The media family on device '%ls' is incorrectly formed. SQL Server cannot process this media family.
- 3242:The file on device '%ls' is not a valid Microsoft Tape Format backup set.
- 3243: The media family on device '%ls' was created using Microsoft Tape Format version %d.%d. SQL Server supports version %d.%d.

These issues can occur due to issues with underlying hardware (hard disks, network storage etc.), virus, malware etc. Review Windows System event logs and hardware logs for errors and take appropriate action (for example: upgrade firmware, fix networking issues etc.)

To solve these issues you need to either locate another usable backup file or create a new backup set. Microsoft does not offer any solutions that can help retrieve data from a corrupt backup set.

Note: If a backup file restores successfully on one server but not on another, try different ways to copy the file between the servers - for example try [robocopy](https://docs.microsoft.com/windows-server/administration/windows-commands/robocopy) instead of a regular copy operation.

### Scheduled backups via maintenance plan or SQL Agent jobs are not working

Majority of the time, backup jobs either created as part of maintenance plan or manually created on the server can fail due to permission issues. Every job step runs in a specific security context. If the job step specifies a proxy, the job step runs in the security context of the credential for the proxy. If a job step does not specify a proxy, the job step runs in the context of the SQL Server Agent service account. So you need to ensure that the corresponding account has Full Control permissions to the folder or network share where the backup files are being written to.  
Note: You can check the owner of a specific job by using SSMS>SQL Server Agent>Jobs>Properties>Steps>Double click each step and check the account under Run as:

### Backup or restore operations that use third-party backup applications are failing

Third party backup applications use Virtual Backup Device Interface (VDI) to backup SQL server databases. Some common troubleshooting steps including the following:

- For SQL Server 2012 and later versions, a new login that is named [NT SERVICE\SQLWriter] is created and provisioned as a login during setup. Make sure that this login exists in SQL Server and is part of the sysadmin server role.
- For versions earlier than SQL Server 2012, make sure that the SQLWriter service is started and that the startup account is set to Local System. Also, make sure that NT AUTHORITY\SYSTEM login exists in SQL Server and that it is part of the sysadmin server role of the instance to which backups are performed.
- Make sure that SqlServerWriter is listed when the VSSADMIN LIST WRITERS command is run at a command prompt on the server that is running SQL Server. This writer must be listed as a writer and should be in the Stable state to enable VSS backups to complete successfully.
- For additional pointers, check the logs from the corresponding backup software and their support sites.

Also review [Backing up a SQL Server database using a VSS backup application may fail for some databases](https://docs.microsoft.com/troubleshoot/sql/admin/backup-database-using-vss-backup-application)

### Issues restoring encrypted databases

If the database master key was encrypted with the service master key, it will be automatically opened when it is needed for decryption or encryption. In this case, it is not necessary to use the OPEN MASTER KEY statement.

When a database is first attached or restored to a new instance of SQL Server, a copy of the database master key (encrypted by the service master key) is not yet stored in the server. You must use the OPEN MASTER KEY statement to decrypt the database master key (DMK). Once the DMK has been decrypted, you have the option of enabling automatic decryption in the future by using the ALTER MASTER KEY REGENERATE statement to provision the server with a copy of the DMK, encrypted with the service master key (SMK). For more information review the following topics:

- [OPEN MASTER KEY](https://docs.microsoft.com/sql/t-sql/statements/open-master-key-transact-sql)
- [RESTORE Statements](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql)

### Unexpected growth of Transaction log files

Under the full recovery model or bulk-logged recovery model, if the transaction log has not been backed up recently, backup might be what is preventing log truncation. If the log has never been backed up, you must create two log backups to permit the Database Engine to truncate the log to the point of the last backup. Truncating the log frees space for new log records. To keep the log from filling up again, take log backups frequently.  
For more information review the following topics:

- [Manage the size of the transaction log file](https://docs.microsoft.com/sql/relational-databases/logs/manage-the-size-of-the-transaction-log-file)
- [Troubleshoot a Full Transaction Log (SQL Server Error 9002)](https://docs.microsoft.com/sql/relational-databases/logs/troubleshoot-a-full-transaction-log-sql-server-error-9002?view=sql-server-ver15#back-up-the-log)

### Issues with compressed backups

A variety of factors impact compression ratio. For more information review [Backup Compression (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/backup-compression-sql-server) and [Behavior of compressed backups when you append backups to an existing media set](https://docs.microsoft.com/troubleshoot/sql/admin/behavior-compressed-backups)

### General troubleshooting tips

- Be sure to provision Read and Write permissions the account running backup job on the folder where the backups are being written to. For more information review [Permissions for backup](https://docs.microsoft.com/sql/t-sql/statements/backup-transact-sql?view=sql-server-ver15#permissions)
- Ensure the folder where the backups are being written to have enough space to accommodate the backups of your databases. You can use sp_spaceused stored procedure to get a rough estimate of size of backup for a specific database.
- Always use latest version of SQL Server Management Studio (SSMS) to ensure you do not run into any known issues related to configuration of jobs and maintenance plans.
- Do a test run of your jobs to ensure the backups are getting created successfully. Always add logic to [verify your backups](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-verifyonly-transact-sql?view=sql-server-ver15).
- If you are looking to move system databases from one server to another review [Move System Databases](https://docs.microsoft.com/sql/relational-databases/databases/move-system-databases?view=sql-server-ver15)
- If you are noticing intermittent backup failures, check if you are running into a issue that is already addressed in a most recent update for your SQL Server version. For more information review [SQL Server Versions and updates](https://docs.microsoft.com/troubleshoot/sql/general/determine-version-edition-update-level)
- Some of the common issues with SQL Server database backup and restore operations can be resolved by referring to the following documents
  - [Troubleshooting SQL Server backup and restore operations](https://docs.microsoft.com/troubleshoot/sql/admin/backup-restore-operations)
  - [Troubleshooting Backup and Restore progress using Extended Events](https://techcommunity.microsoft.com/t5/sql-server/new-extended-event-to-track-backup-and-restore-progress/ba-p/384447)
- To schedule and automate backups for SQL Express editions, review [Schedule and automate backups of SQL Server databases in SQL Server Express](https://docs.microsoft.com/troubleshoot/sql/admin/schedule-automate-backup-database)
