<properties
	pageTitle="BMSUserErrorVaultDeletionNotAllowed"
	description="BMSUserErrorVaultDeletionNotAllowed"
	infoBubbleText="Vault cannot be deleted as there are existing resources within the vault."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-bmsusererrorvaultdeletionnotallowed"
	diagnosticScenario="azurebackup-crc-bmsusererrorvaultdeletionnotallowed"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error BMSUserErrorVaultDeletionNotAllowed

<!--issueDescription-->
We have determined that your operation has failed because the vault cannot be deleted, as there are existing resources within the vault.
<!--/issueDescription-->

## **Recommended Steps**

* Ensure there are no backup items, protected servers, or backup management servers associated with this vault
* Unregister any containers associated with this vault before proceeding for deletion

## **Recommended Document**

* [Delete a Recovery Services Vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)
