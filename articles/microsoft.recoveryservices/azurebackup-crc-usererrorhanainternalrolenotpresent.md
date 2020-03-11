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
	cloudEnvironments="public"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorHANAInternalRoleNotPresent

<!--issueDescription-->
We have identified that your HANA DB backup operation failed because of permission issue.
<!--/issueDescription-->

## **Recommended Steps**

- Ensure AZUREWLBACKUPHANAUSER is present in the HANA system with [required roles and permissions](https://docs.microsoft.com/azure/backup/tutorial-backup-sap-hana-db#setting-up-permissions)
