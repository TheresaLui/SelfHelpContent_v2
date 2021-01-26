<properties
    pageTitle="Domain join command fails since the account name is more than 15 characters in length"
    description="Domain join command fails since the account name is more than 15 characters in length"
    infoBubbleText="Domain join command fails since the account name is more than 15 characters in length"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="25F5C83F-5F79-4D02-B756-2E69B32E0F61"
    ownershipID="StorageMediaEdge_StorageFiles"
/>

# Join-AzStorageAccountForAuth fails when the customer is trying to enable AES256 encryption on the storage account

<!--issueDescription-->
Customer gets the following error while running the Join-AzStorageAccountForAuth command if they are trying to enable AES256 encryption. 

Parameter -StorageAccountName has more than 15 characters, which is not supported to be used as the SamAccountName to create an Active Directory Object. 
 
<!--/issueDescription-->
## **Recommended Action**

This is a known limitation of using AES256 encryption. If you try and domain join a storage account that is longer than 15 characters it will currently fail, you would need to use a storage name shorter than 15 characters or use RC4 encryption instead of AES256. Please ask the to create a storage account which has a name shorter than 15 characters if they want to use AES256 encryption. 

Documentation prerequisites for ADDS Authentication explicitly calls it out: [Overview - On-premises AD DS authentication to Azure file shares](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#supported-scenarios-and-restrictions). 
