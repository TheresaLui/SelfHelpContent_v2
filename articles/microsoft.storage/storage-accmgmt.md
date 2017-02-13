<properties
	pageTitle="How to manage my storage account"
	description="How to manage my storage account"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551643"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
/>

# How to manage my storage account
### **Change your account configuration**
After you create your storage account, you can modify its configuration, such as changing the replication option used for the account or changing the access tier for a Blob storage account. In the Azure portal, navigate to your storage account, click **All settings** and then click **Configuration** to view and/or change the account configuration. 

Changing the replication option will change your pricing. For more details, see [Azure Storage Pricing](https://azure.microsoft.com/pricing/details/storage/) page. 

For Blob storage accounts, changing the access tier may incur charges for the change in addition to changing your pricing. Please see the [Blob storage accounts - Pricing and Billing](https://docs.microsoft.com/azure/storage/storage-blob-storage-tiers#pricing-and-billing) for more details. 

### **Manage your storage access keys**

When you create a storage account, Azure generates two 512-bit storage access keys, which are used for authentication when the storage account is accessed. By providing two storage access keys, Azure enables you to regenerate the keys with no interruption to your storage service or access to that service. 

**View and copy storage access keys**
In the Azure portal, navigate to your storage account, click All settings and then click Access keys to view, copy, and regenerate your account access keys. The Access Keys blade also includes pre-configured connection strings using your primary and secondary keys that you can copy to use in your applications. 

**Regenerate storage access keys**
We recommend that you change the access keys to your storage account periodically to help keep your storage connections secure. Two access keys are assigned so that you can maintain connections to the storage account by using one access key while you regenerate the other access key. 

**Media services** - If you have media services that are dependent on your storage account, you must re-sync the access keys with your media service after you regenerate the keys. 

**Applications** - If you have web applications or cloud services that use the storage account, you will lose the connections if you regenerate keys, unless you roll your keys. 

**Storage Explorers** - If you are using any [storage explorer applications](https://docs.microsoft.com/azure/storage/storage-explorers), you will probably need to update the storage key used by those applications.<br>
Here is the process for rotating your storage access keys: 
1. Update the connection strings in your application code to reference the secondary access key of the storage account.
2. Regenerate the primary access key for your storage account. On the **Access Keys** blade, click Regenerate Key1, and then click Yes to confirm that you want to generate a new key.
3. Update the connection strings in your code to reference the new primary access key.
4. Regenerate the secondary access key in the same manner.


## **Recommended documents**
- [Introduction to Microsoft Azure Storage](https://docs.microsoft.com/azure/storage/storage-introduction)<br>
- [About Azure storage accounts](https://docs.microsoft.com/azure/storage/storage-create-storage-account)<br>
- [Azure Storage Best Practices and Patterns](https://azure.microsoft.com/resources/videos/microsoft-storage-what-new-best-practices-and-patterns/)<br>

