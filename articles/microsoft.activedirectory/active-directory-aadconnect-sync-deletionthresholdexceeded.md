<properties
    pageTitle="Deletion threshold exceeded"
    description="Deletion threshold exceeded"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629775"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="b855b718-b824-476d-a3e2-0e8b8235a606"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Deletion threshold exceeded

## **Recommended Steps**

You may have received an email notification or noticed an error in the **Synchronization Service Manager** UI stating that the number of object deletions has exceeded the configured deletion threshold in Azure AD. This is because of the **Azure AD Connect** feature to prevent any accidental deletions. Here are your options in this case:

* Please follow the [instructions in this document](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-feature-prevent-accidental-deletes) to review the objects to be deleted, disable, or increase the threshold limit.

## **Recommended Documents**

* [Azure AD Connect sync: Prevent accidental deletes](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-feature-prevent-accidental-deletes)
