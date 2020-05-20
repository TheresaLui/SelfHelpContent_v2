<properties
    pageTitle="Synchronizing AD to Azure AD/Synchronization not working"
    description="Synchronizing AD to Azure AD/Synchronization not working"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565591"
    resourceTags=""
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="d23e4390-180d-4024-8eea-23fc48044803"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Synchronizing AD to Azure AD/Synchronization not working

## **Recommended steps**

**Cannot start Azure AD Connect Synchronization Service**

You are unable to start the Synchronization Service in Windows Service Control Manager. Common root causes include the following:

* The Azure AD Connect sync service account, which is used by the Synchronization Service as its security context, has its password changed recently. To resolve this issue, refer to article [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass).

* The Azure AD Connect sync service account is not granted **Logon as a Service** right. For instructions on how to grant this right, refer to article [Add the Logon as a service Right to an Account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions).aspx).

* The Azure AD Connect server is using **LocalDB** as its database, which has a 10-GB limit. When using LocalDB and this limit is reached, the Synchronization Service can no longer start or synchronize properly. To recover from this issue, follow the steps described in article [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit).


**Synchronization Service is started but there is no synchronization activity**

The Azure AD Connect Synchronization Service appears to be running in the Windows Service Control Manager but there is no sychronization activity. Common root causes include the following:

* The Azure Azure Connect wizard is currently open on the Azure AD Connect server. If you start the installation wizard, the scheduler is temporarily suspended until the wizard is closed. For details about this behavior, refer to article section [Azure AD Connect sync: Scheduler - Scheduler and installation wizard](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#scheduler-and-installation-wizard).

* The Azure AD Connect sync scheduler is currently disabled. To verify the status and start the sync scheduler, refer to the steps in article [Azure AD Connect sync: Scheduler](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler).

* The Azure AD Connect server is currently in staging mode. When the Connect server is in staging mode, it will be active for import and synchronization. However, it will not run any exports. For details about staging mode, refer to article section [Azure AD Connect sync: Operational tasks and consideration - Staging mode](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations#staging-mode).


**Synchronization Service cannot import/export changes from on-premises AD**

Common root causes include the following:

* The AD DS account, which is used by the Synchronization Service to communicate with on-premises AD, is either deleted, has its password changed or has its userPrincipalName changed. To resolve this issue, refer to article [Changing the AD DS account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-addsacct-pass).

* The AD DS account does not have the necessary permissions to synchronize changes from on-premises AD. To review the permissions require, refer to article[Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-accounts-permissions).

* There is network connectivity issue between the Azure AD Connect server and on-premises AD. To troubleshoot connectivity issue, refer to article [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity).


**Synchronization Service cannot import/export changes from Azure AD**

Common root causes include the following:

* The Azure AD service account, which is used by the Synchronization Service to communicate with Azure AD, is either deleted, has its password changed or has its userPrincipalName changed. To resolve this issue, refer to article [Azure AD Connect sync: How to manage the Azure AD service account](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass).

* There is network connectivity issue between the Azure AD Connect server and Azure AD. To troubleshoot connectivity issue, refer to article [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity).
