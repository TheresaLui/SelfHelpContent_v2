<properties
    pageTitle="Customer is not able to set NTFS permissions"
    description="Customer is not able to set NTFS permissions"
    infoBubbleText="Customer is not able to set NTFS permissions"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="e1d4c0b4-145e-4aa9-945d-082e55ca55fe"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>


# Customer is not able to set NTFS permissions
<!--issueDescription-->
Customer is not able to set NTFS permissions. They are seeing "An error occurred while applying security information to \\StorageaccountName.file.core.windows.net\FileshareFailed to enumerate objects in the container. Access is denied" error.  

<!--/issueDescription-->

## **Recommended Steps**

* The user needs [**Storage File Data SMB Share Elevated Contributor** RBAC permission]( https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/295083/ADAuth-for-Azure-Files-Access-Denied.md?anchor=things-to-check) on the file share in order to be able to set NTFS permissions. Please use ASC to verify if the user has this RBAC permission.
* If the user does not have this permission, please assign it using the [steps defined here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-assign-permissions#assign-an-rbac-role)

**Note**: To configure NTFS with superuser permissions, user must mount the share by using your storage account key from your domain-joined VM.
