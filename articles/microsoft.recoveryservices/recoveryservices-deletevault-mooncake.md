<properties
	pageTitle="How to delete a Recovery Services vault or Backup vault"
	description="Not able to delete a Backup vault or Recovery Services vault"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anuragm"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>
# Deleting a vault that stores all backup data
There are two types of vaults- Recovery Services vault for Resources Manager deployments and Backup vault for Classic deployment.
## **Recommended steps**
### **Deleting a Recovery Services vault**
1. Open Azure portal and select the vault you want to delete.
2. In the vault view, look at the essentials pane and make sure all entries under Backup Items, Backup management Servers and Replicated Items are zero. If you see non zero, please follow [steps to remove all resources in the Recovery Services vault](https://docs.azure.cn/backup/backup-azure-delete-vault#deleting-a-recovery-services-vault).
3. When there are no more items in the vault, click Delete.
4. When asked to verify that you want to delete the vault, click Yes.
The vault is deleted and the portal returns to the New service menu.

### **Deleting a Backup vault**
1. Open Classic portaland select the vault you want to delete.
2. Look at the number of Windows Servers and/or Azure virtual machines and total storage consumed associated with the vault and make sure the usage is zero. If you see non zero please follow [steps to delete all resources in the Backup vault](https://docs.azure.cn/backup/backup-azure-delete-vault#delete-a-backup-vault).
3. When the usage is zero, click Delete.
4. Select an option on why you are deleting the vault and click checkmark.
The vault is deleted, and you return to the classic portal dashboard.

## **Recommended documents**
[Delete an Azure Backup vault](https://docs.azure.cn/backup/backup-azure-delete-vault)<br>
[Azure Backup FAQs](https://docs.azure.cn/backup/backup-azure-backup-faq)<br>

