<properties
    pageTitle="Unexpected object deletion"
    description="Unexpected object deletion"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629787"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="27a343ca-f725-4702-9002-d90f1d1ef5cb"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Unexpected object deletion

## **Recommended Steps**

You may have received an email notification or noticed an error in the **Synchronization Service Manager** UI stating that the number of object deletions has exceeded the configured deletion threshold in Azure AD. This is because of the **Azure AD Connect** feature that prevents accidental deletions. The following changes can trigger mass deletion of objects, one of which may have caused deletion:

* Changes to filtering where an entire OU or domain is unselected
* All objects in an OU are deleted
* An OU is renamed so all objects in it are now out of scope for synchronization
* Changing the **Scoping filter** of a synchronization rule
* Disabling a synchronization rule which has **Link Type** property value set to provision
* Changing **Link Type** property value of a synchronization rule from provision to join

Please to [review the objects to be deleted, disable, or increase the threshold limit](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-feature-prevent-accidental-deletes).
