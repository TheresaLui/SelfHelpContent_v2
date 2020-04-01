<properties
    pageTitle="Customer sees KRB_AP_ERR_MODIFIED error in the event log"
    description="Customer sees KRB_AP_ERR_MODIFIED error in the event log"
    infoBubbleText="Customer sees KRB_AP_ERR_MODIFIED error in the event log"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public"
    articleId="dec28c79-607e-4152-b724-78b9ffaf4de3"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

<!--issueDescription-->

**Resolution/Workaround**

Dear Customer,

It seems that Storage Account AD object password is out of sync with the kerberos key of your storage account. This could happen f you registered the AD identity/account representing your storage account under an OU that enforces password expiration time. This is currently resulting in authentication failures to access Azure file shares.

To trigger password rotation, you can run the **Update-AzStorageAccountADObjectPassword** command from the AzFilesHybrid module. The cmdlet performs actions similar to storage account key rotation. It gets the second Kerberos key of the storage account and uses it to update the password of the registered account in AD. Then it regenerates the target Kerberos key of the storage account and updates the password of the registered account in AD. You must run this cmdlet in an AD domain joined environment.

Example where action is taken with kerb1:

Update-AzStorageAccountADObjectPassword -ResourceGroupName rgname -StorageAccountName accountname -RotateToKerbKey kerb1
<!--/issueDescription-->