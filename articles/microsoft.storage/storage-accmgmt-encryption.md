<properties
	pageTitle="Troubleshoot Encryption issue"
	description="Troubleshoot Encryption issue"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32691406,32691408,32691409,32691401,32691403,32691404,32691082,32691084,32691085,32691411,32691412,32691413,32691414,32738646"
	resourceTags=""
	productPesIds="15629,16459,16598,16460,16461,16462"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="5b6180d9-a7de-4dd4-9368-3857c71f1c9a"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# How to troubleshoot encryption issue

## **Recommended Documents**

### **Encryption at rest using Customer Managed Key (CMK)**

- [Azure Storage Service Encryption for data at rest](https://docs.microsoft.com/azure/storage/common/storage-service-encryption)
- [Storage Service Encryption using customer-managed keys in Azure Key Vault](https://docs.microsoft.com/azure/storage/common/storage-service-encryption-customer-managed-keys)
- [Encryption at Rest](https://docs.microsoft.com/azure/storage/storage-security-guide#encryption-at-rest)

### **Customer Managed Key (CMK) Auto Key Rotation**

**How often does my key get auto-rotated**?

If the key version is omitted, then Azure Storage checks Azure Key Vault daily for a new version of a customer-managed key. If a new key version is available, then Azure Storage automatically uses the latest version of the key.

**How to setup customer-managed key for auto-rotation?**

- [Specify a key from keyvault](https://docs.microsoft.com/azure/storage/common/storage-encryption-keys-portal#specify-a-key-from-a-key-vault)
- [Configure encryption for automatic rotation of key versions](https://docs.microsoft.com/azure/storage/common/storage-encryption-keys-powershell?toc=/azure/storage/blobs/toc.json#configure-encryption-for-automatic-rotation-of-key-versions)
- [Configure encryption for automatic rotation of key versions ](
https://docs.microsoft.com/azure/storage/common/storage-encryption-keys-cli?toc=/azure/storage/blobs/toc.json#configure-encryption-for-automatic-rotation-of-key-versions)

### **Encryption in transit**

- [Encryption in Transit](https://docs.microsoft.com/azure/storage/storage-security-guide#encryption-in-transit)
- [Enable secure TLS for Azure Storage client](https://docs.microsoft.com/azure/storage/common/storage-security-tls)

### **Disk Encryption**

- [Use Azure Disk Encryption or Storage Service Encryption (SSE) for Disk Encryption](https://docs.microsoft.com/azure/storage/common/storage-security-guide#comparison-of-azure-disk-encryption-sse-and-client-side-encryption)
