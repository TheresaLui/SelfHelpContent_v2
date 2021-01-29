<properties
	pageTitle="Authorization Resource Type Mismatch Error"
	description="Authorization Resource Type Mismatch Error"
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
	articleId="e77c1834-0a0f-4ddf-87be-fac1d788b853"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Authorization Resource Type Mismatch Error

1. Customer uploading files to blob endpoint Azure storage account via Storage Explorer and command line is failing with error Response Status 403 This request is not authorized to perform this operation using this resource type.
2. Due to Invalid SAS token, not set to allow operations on containersobjects. 
3. Create a valid SAS token with permission to the targeted resources e.g. containers and objects. Can be achieved via portal, Storage Explorer etc. [Create a user delegation SAS](httpsdocs.microsoft.comen-usrestapistorageservicescreate-user-delegation-sas)

### Recommended Documents

1. [SAS Error Codes](httpsdocs.microsoft.comen-usrestapistorageservicessas-error-codes)
2. [Internal Wiki](httpssupportability.visualstudio.comAzureVMPOD_wikiwikisAzureVMPOD311345Azure_Storage_TSG_AzCopy-v10-AuthorizationResourceTypeMismatch-Error)
