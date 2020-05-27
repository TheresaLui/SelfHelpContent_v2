<properties
	pageTitle="Troubleshoot issues connecting to Storage service when TLS 1.2 is enabled"
	description="Troubleshoot issues connecting to Storage service when TLS 1.2 is enabled"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32729194,32729195,32729196,32728875"
	productPesIds="15629,16459,16598,16460"
	resourceTags=""
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="storage_common_encryption_tls1.2_enabled"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot issues connecting to Storage service over Azure Private Endpoints

Azure Storage has stopped SSL 3.0 since 2015 and uses TLS 1.2 on public HTTPs endpoints but TLS 1.0 and TLS 1.1 are still supported for backward compatibility.

In order to ensure secure and compliant connection to Azure Storage, you need to enable TLS 1.2 or newer version in client side before sending requests to operate Azure Storage service.

## **Recommended Steps**

Many customers resolved their TLS 1.2 version for Storage service issues using the steps below. This resulted in a faster resolution of the issue and we highly recommend you look through the proposed solutions.

### **Common reasons for connection failures to Storage Service with Private Endpoints**

Below are the common scenarios seen when customers needed help with TLS1.2 enabled.

- [Storage Client connections are failing](https://docs.microsoft.com/azure/storage/common/storage-security-tls?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) - In order to ensure secure and compliant connection to Azure Storage, you need to enable TLS 1.2 or newer version in client side before sending requests to operate Azure Storage service.

- [How to verify TLS version being used by the storage connection](https://docs.microsoft.com/azure/storage/common/storage-security-tls?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#verify-tls-12-connection)

- [Common issues when enabling TLS 1.2](https://docs.microsoft.com/configmgr/core/plan-design/security/enable-tls-1-2-troubleshoot)