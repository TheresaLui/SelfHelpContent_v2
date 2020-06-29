<properties
	pageTitle="How to troubleshoot encryption with CPK issue"
	description="How to troubleshoot encryption with CPK issue"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32691407,32691402,32691083"
	resourceTags=""
	productPesIds="15629,16459,16598"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="7ed78e63-80ea-4040-85a0-797672ce2cd1"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# How to troubleshoot encryption with CPK issue

## **Recommended Documents**

### **Common Support Issues**

- I lost my CPK now what do I do - Azure Storage does not store or manage the encryption key that the client sends with the request. The key is securely discarded as soon as the encryption or decryption process is complete. So, make sure to protect the encryption key that you provide on a request to Blob storage in a secure key store like Azure Key Vault. Unfortunately Azure Support wouldn't be able to help with a lost CPK.  

- [How to rotate CPK](https://docs.microsoft.com/azure/storage/common/storage-service-encryption#rotate-customer-provided-keys)

### **Use CPK with REST API and SDKs**

- [Rest API version 2019-02-02 or higher](https://docs.microsoft.com/rest/api/storageservices/Versioning-for-the-Azure-Storage-Services?redirectedfrom=MSDN#version-2019-02-02)
- [.Net SDK version 11.0.0 or higher](https://github.com/Azure/azure-storage-net/blob/master/Blob/Changelog.txt)
- [Java SDK version 12.0.0-preview.3 or higher](https://github.com/Azure/azure-sdk-for-java/blob/master/sdk/storage/azure-storage-blob/CHANGELOG.md#version-1200-preview3-2019-09-10)

### **Common Error**

- BlobCustomerSpecifiedEncryptionMismatch - Client should provide the exact same encryption key used to encrypt the blob 
- BlobUsesCustomerSpecifiedEncryption - [Client should specify Encryption Headers required with correct encryptions keys to resolve this issue]( https://docs.microsoft.com/azure/storage/common/storage-service-encryption#request-headers-for-specifying-customer-provided-keys)
- InvalidHeaderValue - Client should use the right combination of Encryption Key and its SHA 256 value and use valid key values
