<properties
  pagetitle="Automated backup or managed backup"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="amamun"
  selfhelptype="Generic"
  supporttopicids="32740066"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="37aa2d07-83df-4ce9-9810-a098f1065cbd"
  ownershipid="AzureData_AzureSQLVM" />
# Automated backup or managed backup

## **Recommended Steps**

### Cannot enable Automated backup or managed backup

If you cannot enable Automated backup or managed backup, please ensure following:

- SQL IaaS extension is installed in full mode and is in healthy state
- Account ‘sa’ is not renamed. If you want, you can keep the account at disabled state. 
- Account 'NT Service\SqlIaaSExtensionQuery' has sysadmin privilege in the SQL instance 
- Apply the latest SQL Server patch to avoid any known issues
- User enabling automated backup to form the portal has at least ‘Contributor’ access to the SQL Server machine
- For SQL Server 2016/2017 versions, make sure "Allow Blob Public Access" disabled on Storage Account
- SQL FCI, or multiple named instances do not offer SQL IaaS extension full mode and hence automated backup is not supported

### Backup worked previously but is not working now

If the automated backup or managed backup worked previously but is not working now, please ensure:

- SQL Agent service is in automatic start mode and in started state. You may restart the SQL agent service. 
- SQL Agent service account to be the same as SQL service account to check if it makes a difference

### Known Issues

Please **apply the latest SQL Server patch to avoid any known issues** such as the following. **Latest cumulative update includes all previous fixes.**

- With SQL 2014 , 2016 or 2017 Backup fails with [ErrorCode=(183) Cannot create a file when that file already exists](https://support.microsoft.com/help/4039511/fix-managed-backup-fails-intermittently-because-of-sqlvdi-error-in-sql)
- With SQL 2104, 2016 or 2017, [Managed Backup stops after large database backup in SQL Server](https://support.microsoft.com/help/4040376/fix-managed-backup-to-microsoft-azure-stops-after-large-database-backu)
- With SQL 2016 or 2017 [log backup does not occur as scheduled](https://support.microsoft.com/help/4040535/fix-sql-server-managed-backups-do-not-run-a-scheduled-log-backup-in)
- With SQL 2016 or 2017 [Log chain breaks](https://support.microsoft.com/help/4040530/fix-log-chain-break-in-the-managed-backup-fn-available-backups-table) 
- With SQL 2014 or 2016 [Retention policy does not work](https://support.microsoft.com/help/3168707/fix-retention-policy-does-not-work-when-you-use-sql-server-managed-bac) 
- With SQL 2014 or 2016, [Error Code = 3002, Error Message = Cannot BACKUP or RESTORE a database snapshot apply](https://support.microsoft.com/help/3168708/fix-sql-server-managed-backup-to-windows-azure-tries-to-back-up-databa)
- With SQL 2014, [unable to backup using smart_admin.sp_backup_on_demand](https://support.microsoft.com/help/3169736/fix-can-t-create-a-database-backup-by-executing-smart-admin-sp-backup)

## **Recommended Documents**

* To remove SQL backup files automatically from the blob storage, please review [this article](https://docs.microsoft.com/archive/blogs/ujpat/automate-sql-server-backup-file-removaldeletion-from-azure-blob-storage) 
* To verify current automated backup setting, please review [this article](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/automated-backup#verifysettings)  
* For guidance on automated backup, please follow [SQL 2016+ automated backup](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/automated-backup) or [SQL 2014 automated backup](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/automated-backup-sql-2014) articles
* For guidance on managed backup, please review [SQL Server managed backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-managed-backup-to-microsoft-azure?redirectedfrom=MSDN&view=sql-server-ver15) article
