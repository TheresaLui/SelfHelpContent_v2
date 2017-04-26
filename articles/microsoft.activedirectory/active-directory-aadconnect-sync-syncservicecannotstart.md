<properties
    pageTitle="Cannot start Azure AD Connect Synchronization Service"
    description="Cannot start Azure AD Connect Synchronization Service"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="223"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public"
/>

# Cannot start Azure AD Connect Synchronization Service

## **Recommended steps**
You are unable to start the Synchronization Service in Windows Service Control Manager. Common root causes include the following:

* The Azure AD Connect sync service account, which is used by the Synchronization Service as its security context, has its password changed recently. To resolve this issue, refer to article [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass).

* The Azure AD Connect sync service account is not granted **Logon as a Service** right. For instructions on how to grant this right, refer to article [Add the Log on as a service Right to an Account](https://technet.microsoft.com/library/cc794944(v=ws.10).aspx).

* The Azure AD Connect server is using **LocalDB** as its database, which has a 10-GB limit. When using LocalDB and this limit is reached, the Synchronization Service can no longer start or synchronize properly. To recover from this issue, follow the steps described in article [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit).

## **Recommended documents**
* [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)  
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  
