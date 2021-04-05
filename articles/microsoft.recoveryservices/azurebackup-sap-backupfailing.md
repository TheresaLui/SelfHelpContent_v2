<properties
	pageTitle="Diagnose and resolve issues with SAP HANA Backup is failing"
	description="Diagnose and resolve issues with SAP HANA Backup is failing"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32690765"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8914d3eb-ef72-48b6-aa76-e80246b99342"
	ownershipId="StorageMediaEdge_Backup"
/>

#  When backup of SAP HANA fails follow these troubleshooting steps listed by error code
Use [Backup alerts](https://docs.microsoft.com/azure/backup/sap-hana-db-manage#view-backup-alerts) to know more about the error that you are currently seeing.
## **Recommended Steps**
- [UserErrorInOpeningHanaOdbcConnection – Odbc connection issue](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot#usererrorinopeninghanaodbcconnection)  
- [UserErrorHANALSNValidationFailure – Log chain is broken](https://docs.microsoft.com/en-us/azure/backup/backup-azure-sap-hana-database-troubleshoot#usererrorhanalsnvalidationfailure)
- [UserErrorSDCtoMDCUpgradeDetected – SDC to MDC upgrade](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot#usererrorsdctomdcupgradedetected) 
- [UserErrorInvalidBackintConfiguration – Invalid BackInt configuration](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot#usererrorinvalidbackintconfiguration) 
- [UserErrorBackintCongifUnreadable – BackInt configuration is unreadable](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot#usererrorinvalidbackintconfiguration)
- [UserErrorConfigBadContent – BackInt config bad content](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot#usererrorinvalidbackintconfiguration)
- [UserErrorInsufficientPrivilegeOfDatabaseUser – Database user has insufficient privileges](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot#prerequisites-and-permissions)
- [UserErrorHANAInternalRoleNotPresent –'SAP_INTERNAL_HANA_SUPPORT'role missing on the Workload Backup user](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot#usererrorhanainternalrolenotpresent)

## **Recommended Documents**
- [Frequently asked questions](https://docs.microsoft.com/azure/backup/sap-hana-faq-backup-azure-vm)
- [Troubleshooting issues related to SAP HANA backup in Azure](https://docs.microsoft.com/azure/backup/backup-azure-sap-hana-database-troubleshoot)
