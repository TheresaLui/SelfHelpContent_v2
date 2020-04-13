<properties
	pageTitle="UserErrorRestoreDestinationBlobNotFound"
	description="UserErrorRestoreDestinationBlobNotFound"
	infoBubbleText="Destination blob not found in Restore, likely user deleted it"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorrestoredestinationblobnotfound"
	diagnosticScenario="azurebackup-crc-usererrorrestoredestinationblobnotfound"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorRestoreDestinationBlobNotFound

<!--issueDescription-->
We have identified that your restore operation failed because the target Storage Account or the blob being restored was deleted.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, retry the restore operation on a different storage account and ensure during the restore operation not to delete the selected storage account or any blob associated with this storage account.
