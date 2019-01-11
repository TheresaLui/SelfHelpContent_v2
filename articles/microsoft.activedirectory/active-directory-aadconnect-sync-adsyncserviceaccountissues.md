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
    cloudEnvironments="public"
    />

# ADSync service or service account issues

## **Recommended steps**
You are unable to start the Synchronization Service in Windows Service Control Manager. Common root causes include the following:

* The Azure AD Connect sync service account, which is used by the Synchronization Service as its security context, has its password changed recently. To resolve this issue, refer to article [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass).

* The Azure AD Connect sync service account is not granted **Logon as a Service** right. For more information on how to grant this right, refer to article [Log on as a service](https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/log-on-as-a-service).

* The Azure AD Connect server is using **LocalDB** as its database, which has a 10-GB limit. When using LocalDB and this limit is reached, the Synchronization Service can no longer start or synchronize properly. To recover from this issue, follow the steps described in article [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit).

## **Recommended documents**
* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)  
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  