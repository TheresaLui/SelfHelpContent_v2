<properties
    pageTitle="Unable to set Owner permissions on File share"
    description="Unable to set Owner permissions on File share"
    service="microsoft.storage"
    resource="file storage"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Summary"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public"
    articleId="3983eeb5-a017-43e0-a9ee-ec2dc1586f0e"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to set Owner permissions on File share   

## Symptoms

If the customer tries to change the ownership of a folder located an AD joined file share an error results stating that the user is unable to set new owner on <folder name> (see screenshot below).  

![](Screenshots\UnableToSetOwner.png)

**Error:**  "Unable to set new owner on <file or folder name>"

## Root Cause/Mitigation

This is a known issue during the preview of the Active Directory Authentication for Azure Files feature.  The fix is planned for implementation prior to general availability.

In the meantime, the best way to do this "lift and shift" scenario of **robocopying** files and folders is by accessing the file share through the storage account name and key.

This access is meant to be a "super-user" experience and there will be no access checks when adding files and modifying their ACLs.