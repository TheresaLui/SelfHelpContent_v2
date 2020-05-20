<properties
    pageTitle="Tenant has objects with sync conflict errors"
    description="Tenant has objects with sync conflict errors"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    ms.author="sridhara6"
    authors="sridhara"
    displayOrder="1"
    articleId="Objects_With_Sync_Conflict_Errors"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# AD to AAD Sync
<!--/issueDescription-->
We have identified <!--$ObjectCount-->[ObjectCount]<!--/$ObjectCount--> objects on your tenant <!--$TenantId-->[TenantId]<!--/$TenantId--> that have sync conflict errors.

<!--/issueDescription-->

This could result in the following scenarios:

* You may experience failures when performing licensing related operations on these objects
* You may not be able to update the UserPrincipalName and/or ProxyAddress values on these objects
* You may experience failures when updating MFA settings on these objects
* You may find that objects you synchronized from on-premises AD may not have the correct UserPrincipalName after sync

## **Recommended Steps**

* [Download](https://www.powershellgallery.com/packages/MSOnline/1.1.166.0) and install the Azure AD PowerShell module if you don't already have it installed
* Load the MSOline PowerShell module for Azure AD
* You can identify the list of objects that have sync conflicts by issuing the following commands in a Windows PowerShell console:

  `Connect-MsolService`

  `Get-MsolDirSyncProvisioningError -ErrorCategory PropertyConflict`

* Once you have identified the list of objects, please follow the directions provided in [duplicate or invalid attributes prevent directory synchronization in Office 365](https://support.microsoft.com/help/2647098/duplicate-or-invalid-attributes-prevent-directory-synchronization-in-o) article to resolve those conflicts


## **Recommended Documents**

* Review [known issues](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency#known-issues)
* [Identifying Objects with DirSyncProvisioningErrors](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency#identifying-objects-with-dirsyncprovisioningerrors)
* [Identity synchronization and duplicate attribute resiliency feature](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency)
