<properties
    pageTitle="Customer sees KRB_AP_ERR_MODIFIED error in the event log"
    description="Customer sees KRB_AP_ERR_MODIFIED error in the event log"
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
    articleId="05113e2a-b093-467e-af09-22a963013c5d"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Customer sees KRB_AP_ERR_MODIFIED error in the event log

## Symptoms

If the customer sees "**the target account name is incorrect**" error message or "**net use error 1396**" on their end, please verify if we see the following error message in customer machine's "**System**" event log. 

![](Screenshots\EventLog.jpg)

This issue will appear service account password does not match any of the Kerberos keys of the storage account (ie. kerb1 or kerb2).

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
    
    + Test-AzStorageAccountADObjectPasswordIsKerbKey -ResourceGroupName "psnativerg" …