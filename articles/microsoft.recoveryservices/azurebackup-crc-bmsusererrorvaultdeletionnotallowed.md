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
	cloudEnvironments="public"
/>

# Error BMSUserErrorVaultDeletionNotAllowed

<!--issueDescription-->
We have that your operation failed because the vault cannot be deleted as there are existing resources within the vault.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, ensure there are no backup items, protected servers or backup management servers associated with this vault. Unregister the following containers associated with this vault before proceeding for deletion. For more information refer this [article](https://aka.ms/AB-AA4ecq5)
