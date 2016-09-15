<properties
	pageTitle="How to delete a Recovery Services vault or Backup vault"
	description="Not able to delete a Backup vault or Recovery Services vault"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anuragm"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Delete a Recovery Services vault or Backup vault
The Azure Backup service has two types of vaults - the Backup vault and the Recovery Services vault. The Backup vault came first and can be accessed using classic portal. Then the Recovery Services vault came along to support the expanded Resource Manager deployments and can be accessed from Azure portal. 

## Deleting a Recovery Services vault
Deleting a Recovery Services vault is a one-step process - *provided the vault doesn't contain any resources*. 
* Go to the Recovery Services vault from the Azure portal and click on Delete at the top.
* If you get an error while deleting the vault, please follow [steps to remove or delete all resources in the Recovery Services vault](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-delete-vault/#deleting-a-recovery-services-vault)

## Deleting a Backup vault
Deleting a Backup vault is again a simple process *provided the vault doesn't contain any resources*. 
* Go to the Backup vault from Classis portal and click on Delete at the bottom
* If you get an error while deleting the vault, please follow [steps to remove or delete all resources in the Backup vault](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-delete-vault/#delete-a-backup-vault)

## **Recommended documents**
[Azure Backup FAQs](https://azure.microsoft.com/documentation/articles/backup-azure-backup-faq/)<br>
