<properties
    pageTitle="AD Sync Service or Service Account Issues"
    description="AD Sync Service or Service Account Issues"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629762"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="1c334bfc-e3e7-438f-b43a-34afca40621d"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# ADSync service or service account issues

## **Recommended Steps**

You are unable to start the Synchronization Service in Windows Service Control Manager. Common root causes include the following:

* The Azure AD Connect sync service account, which is used by the Synchronization Service as its security context, has its password changed recently. To resolve this issue, refer to [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass).
* The Azure AD Connect sync service account has not been granted [**Log on as a Service**](https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/log-on-as-a-service) rights
* The Azure AD Connect server is using **LocalDB** as its database, which has a 10GB limit. When using LocalDB and this limit is reached, the Synchronization Service can no longer start or synchronize properly. To recover from this issue, refer to [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit).

## **Recommended Documents**

* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)  
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  
