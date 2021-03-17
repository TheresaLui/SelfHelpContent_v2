<properties
	pageTitle="Troubleshoot Authentication"
	description="Troubleshoot Authentication"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8e237b20-1b9a-4bac-93a4-a5c9260a9568"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check for the customer authorization scenario

## Supported authorization methods 

| Storage type | Authorization method |
|  ------------  |  -------------  |
| Blob storage | Azure AD & SAS | 
| ADLS Gen2 storage | Azure AD & SAS |
| File Storage | SAS only |

### Scoping:

1. What RBAC permissions are assigned?
2. What is the  authentication method (SAS or AAD)?
3. If AAD, did the user log into the correct tenant ID?
4. If SAS, is the token valid? 

Note:

1. For **AAD Auth**, we now support authentication using **User Identity and Service Principal(Client Secret, Certificate)**.
2. All the authentication options, with their examples, are explained **[here](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#choose-how-youll-provide-authorization-credentials)**. Run **"AzCopy Login"** command to authenticate using **AAD Authentication**, otherwise append a SAS token.
3. Ensure proper [**RBAC**](https://docs.microsoft.com/en-us/azure/storage/common/storage-auth-aad-rbac-portal?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) permissions are granted. 
     1. **Storage Blob Data Reader** - read-only 
     2. **Storage Blob Data Owner** - ownership & manage POSIX access for ADLSGen2 
     3. **Storage Blob Data Contributor** - grant read/write/delete 
