<properties
    pageTitle="Import-module -name AzFilesHybrid - Error 'The given assembly name or codebase was invalid'"
    description="Import-module -name AzFilesHybrid - Error 'The given assembly name or codebase was invalid'"
    infoBubbleText="Import-module -name AzFilesHybrid - Error 'The given assembly name or codebase was invalid'"
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
    articleId="56f45929-ab0b-4294-af37-0977c79aa315"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Import-module -name AzFilesHybrid - Error 'The given assembly name or codebase was invalid'

<!--issueDescription-->
Customer gets The given assembly name or codebase was invalid error when trying to import the AzFilesHybrid module. 
<!--/issueDescription-->
## **Recommended Action**
1. Uninstall Az module
2. Ensure that PowerShell 5.1 or above is installed
3. If PowerShell version is not 5.1 or above, upgrade to latest version.* * Install latest Az module version and restart the PowerShell session.
4. Attempt to import AzFilesHybrid Module again.