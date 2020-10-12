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
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="296bcd6b-c2a2-42e2-8dd9-bf0c76bfa996"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup SQL Backup failures

## **Recommended Steps**

- [**UserErrorSQLLSNValidationFailure** - Log chain is broken](https://aka.ms/AB-AA4dwu9) <br>
- [**UserErrorSQLPODoesNotSupportBackupType** - This SQL database does not support the requested backup type](https://aka.ms/AB-usererrorsqlpodoesnotsupportbackuptype)<br>
- [**UserErrorSQLPODoesNotExist** - SQL database does not exist](https://aka.ms/AB-usererrorsqlpodoesnotexist)<br>
- [**UserErrorOpeningSQLConnection** - Azure Backup is not able to connect to the SQL instance](https://aka.ms/AB-usererroropeningsqlconnection)<br>
- [**UserErrorParentFullBackupMissing** - First full backup is missing for this data source](https://aka.ms/AB-usererrorparentfullbackupmissing)<br>
- [**UserErrorBackupFailedAsTransactionLogIsFull** - Cannot take backup as transaction log for the data source is full](https://aka.ms/AB-usererrorbackupfailedastransactionlogisfull)<br>
- UserErrorCannotTakeBackupBasedOnBackupPreference - Ensure all VMs/nodes of the AG are [registered](https://aka.ms/AB-AA4dwug) with Azure Backup. For AG where replica nodes span across Azure geos, ensure nodes in the primary region meet the backup [preference](https://aka.ms/AA4etvp)<br>

## **Recommended Documents**

- [Frequently asked questions](https://aka.ms/AB-AA4dwuc)<br>
- [Troubleshooting issues related to backup SQL Server to Azure](https://aka.ms/AB-AA4dwud)
