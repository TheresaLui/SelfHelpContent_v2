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
    cloudEnvironments="public"
    />

# Synchronization cycle execution issues

## **Recommended Steps**

The synchronization cycle comprised of three steps i.e. import, export and synchronization. Most of time import or export errors lead to synchronization errors.

**Synchronization Issues**

* Use [troubleshooting script to troubleshoot object synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync).

**Import Issues**

There are multiple reasons an object is not importing:

* AD connectivity issues: Please use [ADConnectivityTools](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools) to check connectivity issues with on premise AD. You can [learn more about ADConnectivityTool](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools).

* Azure AD connectivity issues: Please follow instructions in [troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-connectivity).

* AD permissions issues: As a best practice to avoid any permission issues, let Azure AD Connect create accounts instead [providing custom accounts](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions).

* Scoping issue: The object belongs to a [domain or OU which is filtered out](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-configure-filtering) or there is sync rule to filter out the object. 

**Export Issues**

* Data mismatch issue: [Could not find mapping object](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#data-mismatch-errors).

* Duplicate attributes: [Azure AD expects some of attributes to be unique for each object](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#duplicate-attributes).

* Data validation failures: [Azure Active Directory enforces various restrictions on the data](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#data-validation-failures).

* Large object: [Azure Active Directory restrict size limit for some of the attributes](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#largeobject).

* Existing admin role conflict: [Check details about this error here](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#existing-admin-role-conflict).

**Other Issues**

* For advanced troubleshooting go through [this detailed document to check how object flows in AAD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing).

## **Recommended Documents**
* [Troubleshoot object synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync)
* [Azure AD Connect: ADConnectivityTools PowerShell Reference](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools)
* [What is the ADConnectivityTool PowerShell Module?](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools)
* [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools)
* [Troubleshooting errors during synchronization](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors)
* [Azure AD Connect sync: Configure filtering](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-configure-filtering)
* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing)