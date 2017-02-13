<properties
	pageTitle="How to troubleshoot my connectivity or security issue"
	description="How to troubleshoot my connectivity or security issue"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551655"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
/>

# How to troubleshoot my connectivity or security issue
### **Connectivity**
1. Solutions to connect to a storage account to store images:
   - [Microsoft Azure Storage Explorer](http://storageexplorer.com)
   - [PowerShell](https://azure.microsoft.com/documentation/articles/storage-powershell-guide-full/)
2. Information about [Azure Storage Connection Strings can be found in this article](https://docs.microsoft.com/azure/storage/storage-configure-connection-string)

### **Security**
The storage account itself can be secured using Role-Based Access Control and Azure Active Directory. Data can be secured in transit between an application and Azure by using [Client-Side Encryption](https://azure.microsoft.com/documentation/storage-client-side-encryption.md), HTTPS, or SMB 3.0. Data can be set to be automatically encrypted when written to Azure Storage using [Storage Service Encryption (SSE)](https://docs.microsoft.com/azure/storage/storage-service-encryption). OS and Data disks used by virtual machines can be set to be encrypted using [Azure Disk Encryption](https://docs.microsoft.com/azure/security/azure-security-disk-encryption). Delegated access to the data objects in Azure Storage can be granted using [Shared Access Signatures](https://azure.microsoft.com/documentation/articles/storage-dotnet-shared-access-signature-part-1/).

**Azure Storage Security Options:**
* [Management Plane Security](https://docs.microsoft.com/azure/storage/storage-security-guide#management-plane-security) – Securing your Storage Account
* [Data Plane Security](https://docs.microsoft.com/azure/storage/storage-security-guide#data-plane-security) – Securing Access to Your Data
* [Encryption in Transit](https://docs.microsoft.com/azure/storage/storage-security-guide#encryption-in-transit)
* [Encryption at Rest](https://docs.microsoft.com/azure/storage/storage-security-guide#encryption-at-rest)
* Using [Storage Analytics](https://docs.microsoft.com/azure/storage/storage-security-guide#storage-analytics) to audit access of Azure Storage
* [Enabling Browser-Based Clients using CORS](https://docs.microsoft.com/azure/storage/storage-security-guide#Cross-Origin-Resource-Sharing-CORS)

## **Recommended documents**
- [Azure Storage security guide](https://docs.microsoft.com/azure/storage/storage-security-guide)
- [Security Access using Shared Access Signature (SAS)](https://azure.microsoft.com/documentation/articles/storage-dotnet-shared-access-signature-part-1/)
- [Use role assignments to manage access to your Azure subscription resources](https://azure.microsoft.com/documentation/articles/role-based-access-control-configure/)
- [User Policy to manage resources and control access](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy)
- [For a specific read access to a set of Users](https://docs.microsoft.com/rest/api/storageservices/fileservices/Service-SAS-Examples?redirectedfrom=MSDN)
- [Cross-Origin Resource Sharing (CORS) for Azure storage](https://docs.microsoft.com/rest/api/storageservices/fileservices/cross-origin-resource-sharing--cors--support-for-the-azure-storage-services)
- [Generate SAS Tokens using Storage Explorer](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer)
- [Manage Storage Keys](https://docs.microsoft.com/azure/storage/storage-create-storage-account)
- [Azure Storage Connection Strings](https://docs.microsoft.com/azure/storage/storage-configure-connection-string)
