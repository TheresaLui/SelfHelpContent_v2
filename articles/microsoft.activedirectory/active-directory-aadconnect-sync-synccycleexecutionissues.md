<properties
    pageTitle="Sync cycle execution issues"
    description="Sync cycle execution issues"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629805"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="8d6ad72d-004d-405b-ab2c-e9fa8ed83357"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Synchronization cycle execution issues

## **Recommended Steps**

The synchronization cycle has three steps: import, export, and synchronization. Import or export errors can frequently lead to synchronization errors.

**Synchronization Issues**

* Use a [troubleshooting script](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync) to troubleshoot object synchronization with Azure AD Connect sync

**Import Issues**

There are multiple reasons why an object is not importing:

* AD connectivity issues: Please use [ADConnectivityTools](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools) to check connectivity issues with on premise AD
* Azure AD connectivity issues: Please follow instructions to [troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-connectivity)
* AD permissions issues: As a best practice to avoid any permission issues, let Azure AD Connect [create accounts instead of providing custom accounts](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* Scoping issue: The object belongs to a [domain or OU which is filtered out](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-configure-filtering) or there is sync rule to filter out the object

**Export Issues**

* Data mismatch issue: [Could not find mapping object](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#data-mismatch-errors)
* Duplicate attributes: [Azure AD expects some attributes to be unique for each object](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#duplicate-attributes)
* Data validation failures: [Azure Active Directory enforces various restrictions on the data](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#data-validation-failures)
* Large object: [Azure Active Directory restricts size limit for some attributes](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#largeobject)
* [Existing admin role conflict](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#existing-admin-role-conflict)

**Other Issues**

* For advanced troubleshooting, [review how objects flow in AAD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing)

## **Recommended Documents**

* [Troubleshoot object synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync)
* [Azure AD Connect: ADConnectivityTools PowerShell Reference](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools)
* [What is the ADConnectivityTool PowerShell Module?](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools)
* [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools)
* [Troubleshooting errors during synchronization](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors)
* [Azure AD Connect sync: Configure filtering](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-configure-filtering)
* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing)
 
