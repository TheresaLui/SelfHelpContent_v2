<properties
                pageTitle="Azure Backup SQL Backup failures"
                description="Azure Backup SQL Backup failures"
                service="microsoft.recoveryservices"
                resource="vaults"
                authors="srinathv"
		ms.author="srinathv"
                displayOrder=""
                selfHelpType="generic"
                supportTopicIds="32605791"
                resourceTags=""
                productPesIds="15207"
                cloudEnvironments="public"
	articleId="296bcd6b-c2a2-42e2-8dd9-bf0c76bfa996"
/>

# Azure Backup SQL Backup failures

## **Recommended steps**
- [**UserErrorSQLLSNValidationFailure** - Log chain is broken](https://aka.ms/AB-AA4dwu9) </br>
- **UserErrorCannotTakeBackupBasedOnBackupPreference** - Ensure all VMs/nodes of the AG are [registered](https://aka.ms/AB-AA4dwug) with Azure Backup. For AG where replica nodes span across Azure geos, ensure nodes in the primary region meet the backup [preference](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-properties-new-availability-group-backup-preferences-page) </br>

## **Recommended Documents**
- [FAQs](https://aka.ms/AB-AA4dwuc)</br>
- [Troubleshooting issues related to back up SQL Server to Azure](https://aka.ms/AB-AA4dwud)</br>
