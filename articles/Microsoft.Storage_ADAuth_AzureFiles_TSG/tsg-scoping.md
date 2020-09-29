<properties
    pageTitle="Scope the issue customer faces"
    description="Scope the issue customer faces"
    service="Microsoft.Storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="c0908a98-70fe-4f51-b116-4f8a04e2fc29"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Scope customer issue accurately

## Make sure you completely understand the customer scenario
1. Did the customer run through all the [prerequisites](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-domain-service-enable#prerequisites)? Verify using scoping questions on the case.
2. Has the customer already enabled AD Authentication on the storage account? Verify using ASC. 
3. Is the customer able to successfully mount the share using storage account key?
4. Is the customer able to successfully mount the share using their own identity? 
5. Is the customer facing issues while setting up NTFS permissions?
6. Is the customer facing issues while accessing the individual files? 
7. It is also important to know exactly **when did the issue occur**. Grab the exact timestamp of the issue when it last happened. 

## Data Collection
1. Use ASC to verify if the customer was able to enable the feature on the account. 
2. If the feature is not enabled, ask the customer to share the result of running the Hybrid PowerShell module and share all the commands they ran.
3. If the feature is enabled, ask the customer to share the following. 
      
    i. Result of "whoami /user" & "whoami /groups" command

    ii. NTFS permissions on the file/directory using the "icacls file/directory" command.  

    iii. OID of the user.

    iv. Kerberos ticket of the storage account using "**Get-AzStorageKerberosTicketStatus**" command of the Hybrid PowerShell module.