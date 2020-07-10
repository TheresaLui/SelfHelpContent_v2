<properties
    pageTitle="Unable to mount - CheckADObjectPasswordIsCorrect check fails"
    description="Unable to mount - CheckADObjectPasswordIsCorrect check fails"
    infoBubbleText="Unable to mount - CheckADObjectPasswordIsCorrect check fails"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="dec28c79-607e-4152-b724-78b9ffaf4de3"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to mount - CheckADObjectPasswordIsCorrect check fails
<!--issueDescription-->
In order for AD Auth to work properly, password configured on the storage AD identity needs to match one of the storage account kerb keys.
<!--/issueDescription-->


## **Recommended Steps**

1. Please work with the customer to update password of the storage account AD object by following the guidance below. 

2. Once the password has been updated successfully, re-run the "Debug-AzStorageAccountAuth" cmdlet to make sure all the other checks pass successfully. If they do not, go back to previous step to further troubleshoot. 

3. If "Debug-AzStorageAccountAuth" completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate.

**Customer Ready Message**

Dear Customer,

It seems that Storage Account AD object password is out of sync with the kerberos key of your storage account. This could happen if you registered the AD identity representing your storage account under an OU that enforces password expiration time. This is currently resulting in authentication failures to access Azure file shares.

To trigger password rotation, you can run  Update-AzStorageAccountADObjectPassword command from the AzFilesHybrid module. The cmdlet performs actions similar to storage account key rotation. It gets the second Kerberos key of the storage account and uses it to update the password of the registered account in AD. Then it regenerates the target Kerberos key of the storage account and updates the password of the registered account in AD. You must run this cmdlet in an AD domain joined environment.

Example where action is taken with kerb1:

Update-AzStorageAccountADObjectPassword -ResourceGroupName rgname -StorageAccountName accountname -RotateToKerbKey kerb1