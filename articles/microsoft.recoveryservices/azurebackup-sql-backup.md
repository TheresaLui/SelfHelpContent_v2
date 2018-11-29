<properties
                pageTitle="Azure Backup SQL Backup failures"
                description="Azure Backup SQL Backup failures"
                service="microsoft.recoveryservices"
                resource="vaults"
                authors="srinathvasireddy"
                displayOrder=""
                selfHelpType="generic"
                supportTopicIds="32605791"
                resourceTags=""
                productPesIds="15207"
                cloudEnvironments="public"
/>

# Azure Backup SQL Backup failures

## **Recommended steps**
- [**UserErrorSQLLSNValidationFailure** - Log chain is broken](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorsqllsnvalidationfailure) </br>
- **UserErrorCannotTakeBackupBasedOnBackupPreference** - Ensure all VMs/nodes of the AG are [registered](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#discover-sql-server-databases) with Azure Backup. For AG where replica nodes span across Azure geos, ensure nodes in the primary region meet the backup [preference](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-properties-new-availability-group-backup-preferences-page) </br>

## **Recommended Documents**
- [FAQs](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#faq)</br>
- [Troubleshooting issues related to back up SQL Server to Azure](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot)</br>
