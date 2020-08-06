<properties
    pageTitle="Import-module -name AzFilesHybrid - Error 'Unable to uninstall the GA version of the Az.Storage module'"
    description="Import-module -name AzFilesHybrid - Error 'Unable to uninstall the GA version of the Az.Storage module'"
    infoBubbleText="Import-module -name AzFilesHybrid - Error 'Unable to uninstall the GA version of the Az.Storage module'"
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
    articleId="fc786be5-4537-494d-a5b9-ea5c08348246"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Import-module -name AzFilesHybrid - Error 'Unable to uninstall the GA version of the Az.Storage module'

<!--issueDescription-->
Customer gets the following error while trying to import AzFilesHybrid module - Unable to uninstall the GA version of the Az.Storage module
<!--/issueDescription-->

## **Recommended Steps**

Please follow below steps to resolve customer issues when they get this error while trying to Import Hybrid PowerShell module. 

1. Ensure that the latest version of the PowerShellGet Module is installed: `Install-Module -Name PowerShellGet -Force`
2. Install Az.Storage module version 2.0.0 manually: `Install-Module -Name Az.Storage -RequiredVersion 2.0.0 -AllowPrerelease`
3. Restart the PowerShell Session
4. Attempt to import the AzFilesHybrid module again
