<properties
	pageTitle="BMSUserErrorVaultDeletionNotPermitted"
	description="BMSUserErrorVaultDeletionNotPermitted"
	infoBubbleText="Recovery Services vault cannot be deleted as there are backup items in soft deleted state in the vault."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-bmsusererrorvaultdeletionnotpermitted"
	diagnosticScenario="azurebackup-crc-bmsusererrorvaultdeletionnotpermitted"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error BMSUserErrorVaultDeletionNotPermitted

<!--issueDescription-->
We have identified that your Recovery Services vault cannot be deleted as there are backup items in soft deleted state in the vault.
<!--/issueDescription-->

## **Recommended Steps**

To delete the Recovery Services vault it should meet the following conditions: 

- There should not be any protected items in the vault
- There should not be any soft deleted items in the vault
- If you do have soft deleted items in the vault, then wait for 14 days for expiration of soft deleted items and retry the operation

## **Recommended Document**

* To disable the soft delete feature for newly created vaults, refer to [Disabling Soft Delete](https://go.microsoft.com/fwlink/?linkid=2111043)
