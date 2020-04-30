<properties
    pageTitle="How to delete a Recovery Services vault or Backup vault"
    description="Not able to delete a Backup vault or Recovery Services vault"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="anuragm"
    ms.author="anuragm"
    displayOrder="7"
    selfHelpType="generic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="5f701380-150c-410b-a192-966fc38a03c6"
	ownershipId="Compute_SiteRecovery"
/>

# I want to delete a vault that stores backup data

There are two types of vaults: **Recovery Services vault** for Resources Manager deployments, and **Backup vault** for Classic deployment.

## **Recommended Steps**

### **Deleting a Recovery Services vault**

1. Open [Azure portal](https://portal.azure.com) and select the vault you want to delete
2. In the vault view, look at the essentials pane and make sure all entries under Backup Items, Backup management Servers, and Replicated Items are zero. If you see a number other than zero, please follow the [steps to remove all resources in the Recovery Services vault](https://docs.azure.cn/backup/backup-azure-delete-vault#deleting-a-recovery-services-vault).
3. When there are no more items in the vault, click Delete
4. When asked to verify that you want to delete the vault, click Yes

The vault is deleted and the portal returns to the New service menu.

### **Deleting a Backup vault**

1. Open Classic portal and select the vault you want to delete
2. Look at the number of Windows Servers and/or Azure virtual machines and total storage consumed associated with the vault, and make sure the usage is zero. If you see a number other than zero, please follow the [steps to delete all resources in the Backup vault](https://docs.azure.cn/backup/backup-azure-delete-vault#delete-a-backup-vault).
3. When the usage is zero, click Delete
4. Select an option on why you are deleting the vault and click checkmark

The vault is deleted, and you return to the classic portal dashboard.

## **Recommended Documents**

* [Delete an Azure Backup vault](https://docs.azure.cn/backup/backup-azure-delete-vault)<br>
* [Azure Backup FAQs](https://docs.azure.cn/backup/backup-azure-backup-faq)
