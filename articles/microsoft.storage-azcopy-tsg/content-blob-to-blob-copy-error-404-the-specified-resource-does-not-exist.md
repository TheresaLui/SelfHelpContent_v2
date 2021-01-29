<properties
	pageTitle="Blob to Blob copy error 404 The specified resource does not exist."
	description="Blob to Blob copy error 404 The specified resource does not exist."
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
	articleId="8a79ab98-bbc9-44ad-a17f-c26a8126e2af"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Blob to Blob copy error 404 The specified resource does not exist.

1. Scenario: Error while attempting to copy a blob from one storage account to another, using AAD for authentication (OAuth 2.0) you get an error.
2. Solution
    1. In the current release, you must **append a SAS token to each source URL.** 
    2. If you provide authorization credentials by using **Azure Active Directory (AAD)**, you can **omit** the SAS token only from the **destination URL**.

~~~shell

azcopy cp "https://$source-storage-account-name$.blob.core.windows.net/$container-name$/$blob-path$**?$SAS-token$**" "https://$destination-storage-account-name$.blob.core.windows.net/$container-name$/$blob-path$"

~~~

## Recommended Documents

1. [See other Authorization TSGs](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=authorization-related-tsgs) for more info. 

