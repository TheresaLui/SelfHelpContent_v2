<properties
	pageTitle="BMSUserErrorVaultDeletionForbidden"
	description="BMSUserErrorVaultDeletionForbidden"
	infoBubbleText="Vault cannot be deleted as there are existing resources including backup items in soft deleted state within the vault."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-bmsusererrorvaultdeletionforbidden"
	diagnosticScenario="azurebackup-crc-bmsusererrorvaultdeletionforbidden"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error BMSUserErrorVaultDeletionForbidden

<!--issueDescription-->
We have determined that your operation has failed because the vault cannot be deleted, as there are existing resources, including backup items, in soft deleted state within the vault.
<!--/issueDescription-->

## **Recommended Steps**

* Ensure there are no backup items, protected servers, or backup management servers associated with this vault. [Learn more](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#before-you-start).
* [Unregister any containers associated with this vault before proceeding for deletion](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#proper-way-to-delete-a-vault)
* If you do have soft deleted items in the vault, either wait for 14 days for expiration of soft deleted items and retry the operation, or follow these steps for [permanently deleting soft deleted backup items](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud#permanently-deleting-soft-deleted-backup-items)

## **Recommended Document**

* To disable the soft delete feature for newly created vaults, see [disabling soft delete](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud#disabling-soft-delete)
* See [step-by-step instructions to delete a Recovery Services Vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)
