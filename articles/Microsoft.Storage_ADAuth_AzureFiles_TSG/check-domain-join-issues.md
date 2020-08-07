<properties
    pageTitle="Customer is facing domain join issues"
    description="Customer is facing domain join issues"
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
    articleId="d0058d2c-7cd3-48b2-a09c-6aa256f8eb67"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Customer is facing domain join issues

If Join-AzStorageAccountForAuth script does not work as expected, verify the state of customer environment.Specifically, you must check if [Active Directory PowerShell](https://docs.microsoft.com/powershell/module/addsadministration/?view=win10-ps) is installed, and if the shell is being executed with administrator privileges. Then check to see if the [Az.Storage 2.0 module](https://www.powershellgallery.com/packages/Az.Storage/2.0.0) is installed, and install it if it isn't.

Once verified that the customer has right environment setup, please ask them to run the Join command using '-verbose' option and share the result.
