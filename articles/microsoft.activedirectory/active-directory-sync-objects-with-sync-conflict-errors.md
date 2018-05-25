<properties
    pageTitle="Tenant has objects with sync conflict errors"
    description="Tenant has objects with sync conflict errors"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sridhara"
    displayOrder="1"
    articleId="Objects_With_Sync_Conflict_Errors"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# AD to AAD Sync

We have identified <!--$ObjectCount-->[ObjectCount]<!--/$ObjectCount--> objects on your tenant <!--$TenantId-->[TenantId]<!--/$TenantId--> that have sync conflict errors. This could impact the following scenarios:

*   You may experience failures when performing licensing related operations on these objects.
*   You may not be able to update the UserPrincipalName and/or ProxyAddress values on these objects.
* You may experience failures when updating MFA settings on these objects.
*   You may find that objects you synchronized from on-premises AD may not have the correct UserPrincipalName after sync.

We recommend that you review the [Identity synchronization and duplicate attribute resiliency feature](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency).

You can identify the list of objects that have sync conflicts by issuing the following commands in a Windows PowerShell console after loading MSOnline PowerShell module for Azure AD version 1.1.166.0.  Please [download](https://www.powershellgallery.com/packages/MSOnline/1.1.166.0) and install the Azure AD PowerShell module if you don't already have it installed.

Connect-MsolService

Get-MsolDirSyncProvisioningError -ErrorCategory PropertyConflict

You can find more information on using this command by referring to [Identifying Objects with DirSyncProvisioningErrors](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency#identifying-objects-with-dirsyncprovisioningerrors) article.

Once you have identified the list of objects, please follow the directions provided in [duplicate or invalid attributes prevent directory synchronization in Office 365](https://support.microsoft.com/en-us/help/2647098/duplicate-or-invalid-attributes-prevent-directory-synchronization-in-o) article to resolve those conflicts.

Also please review [known issues](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency#known-issues).

Please let me know if you have any questions or concerns.