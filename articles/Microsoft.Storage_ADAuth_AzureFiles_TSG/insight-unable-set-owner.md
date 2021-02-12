<properties
    pageTitle="Unable to set Owner permissions on File share"
    description="Unable to set Owner permissions on File share"
    infoBubbleText="Unable to set Owner permissions on File share"
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
    articleId="3983eeb5-a017-43e0-a9ee-ec2dc1586f0e"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to set Owner permissions on File share

<!--issueDescription-->
If the customer tries to change the ownership of a folder located an AD joined file share an error results stating that the user is unable to set new owner on file share.  

Error:  "Unable to set new owner on share name. Access is denied."

This is a known issue of the Active Directory Authentication for Azure Files feature.  The fix is planned for implementation.

Customer Ready Message

Hello Customer, 

Due to a known issue of the Active Directory Authentication for Azure Files feature, users will not be able to change the ownership of a folder located on AD enabled Azure File Share. 

In the meantime, the best way to achieve any scenarios where super experience is required ("lift and shift" scenario of robocopying files and folders),  is by accessing the file share through the storage account name and key.

This access is meant to be a "super-user" experience and there will be no access checks when adding files and modifying their ACLs.

<!--/issueDescription-->
