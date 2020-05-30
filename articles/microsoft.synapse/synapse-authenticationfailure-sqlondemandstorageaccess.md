<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738811"
	displayOrder = ""
	diagnosticScenario = ""
	pageTitle = "Authentication failure/SQL on-demand storage access"
	description = "Authentication failure/SQL on-demand storage access"
	infoBubbleText = ""
	articleId = "synapse-authenticationfailure-sqlondemandstorageaccess"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>

# Authentication failure/SQL on-demand storage access

## **Recommended Steps**

* If your query fails with the error message 'File cannot be opened because it does not exist or it is used by another process' and you're sure both file exist and it's not used by another process, it means SQL on-demand can't access the file. 

* If you are using AAD login, check whether UserIdentity credential exists. If it exists, check if you have proper rights to access the file. Easiest way is to grant yourself 'Storage Blob Data Contributor' role on the storage account you're trying to query. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal). 

* For credentials defined on storage path level, make sure credential is not created on storage level, but at least on container level. For more information see [control storage access for SQL on-demand](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control). 

* Check if proper credential is created as described in [control storage access for SQL on-demand](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control). 

* If using ADF to access SQL on-demand, check if MSI account for your workspace is given access to storage. MSI account has the same name as your workspace name. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal). 



