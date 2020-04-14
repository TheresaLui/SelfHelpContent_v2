<properties
	pageTitle="UserErrorHANAInternalRoleNotPresent"
	description="UserErrorHANAInternalRoleNotPresent"
	infoBubbleText="Workload Backup User (eg: AZUREWLBACKUPHANAUSER) doesn't have required role(SAP_INTERNAL_HANA_SUPPORT) assigned"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorhanainternalrolenotpresent"
	diagnosticScenario="azurebackup-crc-usererrorhanainternalrolenotpresent"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorHANAInternalRoleNotPresent

<!--issueDescription-->
We have identified that your HANA DB backup operation failed because of permission issue.
<!--/issueDescription-->

## **Recommended Steps**

- Ensure AZUREWLBACKUPHANAUSER is present in the HANA system. 
- Re-run the [pre-registration script](https://download.microsoft.com/download/B/2/E/B2E01EF8-C247-42A6-BCC7-E45B78F20C99/msawb-plugin-config-com-sap-hana.sh) to resolve the permissions issue

## **Recommended Document**
[What the pre-registration script does](https://docs.microsoft.com/azure/backup/tutorial-backup-sap-hana-db#what-the-pre-registration-script-does)

