<properties
	pageTitle="UserErrorInvalidAuthenticationTokenTenant"
	description="UserErrorInvalidAuthenticationTokenTenant"
	infoBubbleText="the restore operation failed because the subscription is transferred to another tenant."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorinvalidauthenticationtokentenant"
	diagnosticScenario="azurebackup-crc-usererrorinvalidauthenticationtokentenant"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorInvalidAuthenticationTokenTenant

<!--issueDescription-->
We have identified that the restore operation failed because the subscription is transferred to another tenant.
<!--/issueDescription-->

## **Recommended Steps**

- In this case, Original Location Restore is not supported. Use [Alternate Location Restore](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#before-you-start) or [restore disk](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-disks) options
