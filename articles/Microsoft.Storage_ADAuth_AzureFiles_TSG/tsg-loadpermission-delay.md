<properties
    pageTitle="Loading of the add permissions window takes longer than expected"
    description="Loading of the add permissions window takes longer than expected"
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
    articleId="de10218f-46fd-4bb0-94f8-2c4c0bc5955e"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Loading of the add permissions window takes longer than expected 

## Symptoms

Load the permissions window for files or folders takes a long time (typically over 20 seconds).

![](Screenshots\LoadPermissionsDelay.png)

## Root Cause/Mitigation

This is a known issue during the preview of the Active Directory Authentication for Azure Files feature.  The fix is planned for implementation prior to general availability.