<properties
    pageTitle="Debug command fails during CheckStorageAccountDomainJoined step"
    description="Debug command fails during CheckStorageAccountDomainJoined step"
    infoBubbleText="Debug command fails during CheckStorageAccountDomainJoined step"
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
    articleId="e336596d-16aa-435e-b7bd-c6a5f208659a"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Debug command fails during CheckStorageAccountDomainJoined step

<!--issueDescription-->
Debug command fails during CheckStorageAccountDomainJoined step
<!--/issueDescription-->

## **Recommended Steps**

1. This error means that the customer does not have AD authentication enabled on the storage account and the account's AD properties are populated
2. Please ask the customer to re-run "Join-AzStorageAccountForAuth" command to re-enable AD Auth on the storage account
3. Once they have successfully run "Join-AzStorageAccountForAuth", re-run the "Debug-AzStorageAccountAuth" cmdlet to make sure all the other checks pass successfully. If they do not, go back to previous step to further troubleshoot.
4. If "Debug-AzStorageAccountAuth" completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate.
