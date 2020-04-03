<properties
    pageTitle="CopytoPSPath.ps1 - Error 'The term 'Import-PowerShellDataFile' is not recognized'"
    description="CopytoPSPath.ps1 - Error 'The term 'Import-PowerShellDataFile' is not recognized'"
    infoBubbleText="CopytoPSPath.ps1 - Error 'The term 'Import-PowerShellDataFile' is not recognized'"
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
    articleId="56f45929-ab0b-4294-af37-0977c79aa315"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# The term Import-PowerShellDataFile is not recognized
<!--issueDescription-->
Please follow below steps to resolve customer issues when they get this error while trying to run CopytoPSPath.ps1 command. 
<!--/issueDescription-->

## **Recommended Steps**

1. Check .Net version by looking at the "Version" registry key under this path - HKEY_LOCAL_MACHINE-SOFTWARE-Microsoft-NET Framework Setup-NDP-v4-Full 
2. Run "$PSVersionTable.PSVersion" from a PowerShell Console to verify the PowerShell version. 
3. If either .Net or PowerShell do not meet minimum requirements, instruct the customer on how to upgrade and retry.