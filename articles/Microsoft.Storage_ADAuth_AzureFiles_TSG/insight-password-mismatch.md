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
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="dec28c79-607e-4152-b724-78b9ffaf4de3"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Customer sees KRB_AP_ERR_MODIFIED error in the event log
<!--issueDescription-->
Customer sees KRB-AP-ERR-MODIFIED error in the event log
<!--/issueDescription-->


## **Recommended Steps**

We've added a new method "**Test-ADPasswordMatchesAccountKerbKey**" to the PowerShell module that checks for this condition of the out-of-sync password.

Output that shows the AD password for the storage account matches one of the kerb keys:

    PS C:\> Test-AzStorageAccountADObjectPasswordIsKerbKey -ResourceGroupName "psnativerg" -Name "lesliefrancetest" -Verbose
    VERBOSE: Found that kerb1 matches password for lesliefrancetest in AD.
    True

Output that shows the AD password for the storage account does not match one of the kerb keys:
            
    PS C:\> Test-AzStorageAccountADObjectPasswordIsKerbKey -ResourceGroupName "psnativerg" -Name "lesliefrancetest" -Verbose
    Test-AzStorageAccountADObjectPasswordIsKerbKey : Password for canarynativead\lesliefrancetest does not match kerb1 or kerb2 of storage account: lesliefrancetest
        Please run the following command to resync the AD password with the kerb key of the storage account and retry.
        
        Update-AzStorageAccountAdObjectPassword -ResourceGroupName <resourceGroupName> -StorageAccountName <storageAccountName> -RotateToKerbKey kerb1
        
    At line: 1 char:1
    
    + Test-AzStorageAccountADObjectPasswordIsKerbKey -ResourceGroupName "psnativerg"

Please follow below action plan if the customer faces the above specified error message. 

**Customer Ready Message**

Dear Customer,

It seems that Storage Account AD object password is out of sync with the kerberos key of your storage account. This could happen if you registered the AD identity representing your storage account under an OU that enforces password expiration time. This is currently resulting in authentication failures to access Azure file shares.

To trigger password rotation, you can run  Update-AzStorageAccountADObjectPassword command from the AzFilesHybrid module. The cmdlet performs actions similar to storage account key rotation. It gets the second Kerberos key of the storage account and uses it to update the password of the registered account in AD. Then it regenerates the target Kerberos key of the storage account and updates the password of the registered account in AD. You must run this cmdlet in an AD domain joined environment.

Example where action is taken with kerb1:

Update-AzStorageAccountADObjectPassword -ResourceGroupName rgname -StorageAccountName accountname -RotateToKerbKey kerb1