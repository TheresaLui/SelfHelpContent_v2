<properties
    pageTitle="Unable to mount - Storage Account's AD object is missing in On-Prem Active Directory"
    description="Unable to mount - Storage Account's AD object is missing in On-Prem Active Directory"
    infoBubbleText="Unable to mount - Storage Account's AD object is missing in On-Prem Active Directory"
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
    articleId="7af24444-f9b2-4980-9988-cffc93fa3ccf"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to mount - Storage Account's AD object is missing in On-Prem Active Directory
<!--issueDescription-->
In order for AD Auth to work properly, the logged on user needs to have a valid AD Object associated with the storage account they are trying to connect to.
<!--/issueDescription-->

## **Recommended Steps**

1. Please work with the customer to recreate the AD Object using "Join-AzStorageAccountForAuth" cmdlet or manually using the steps [defined here](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-enable#creating-an-identity-representing-the-storage-account-in-your-ad-manually). Please run the "Join-AzStorageAccountForAuth" cmdlet with "-verbose" option in order to see if the customer is facing any issues creating this AD Object. 
2. Once the AD Object is created successfully, re-run the "Debug-AzStorageAccountAuth" cmdlet to make sure all the other checks pass successfully. If they do not, go back to previous step to further troubleshoot. 
3. If "Debug-AzStorageAccountAuth" completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate.