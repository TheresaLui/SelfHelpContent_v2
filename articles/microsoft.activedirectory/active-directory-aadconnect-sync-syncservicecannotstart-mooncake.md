<properties
    pageTitle="Cannot start Azure AD Connect Synchronization Service"
    description="Cannot start Azure AD Connect Synchronization Service"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    ms.author="cychua"
    displayOrder="49"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect,directory_overview"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-aadconnect-sync-syncservicecannotstart-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Cannot start Azure AD Connect Synchronization Service

## **Recommended Steps**

You are unable to start the Synchronization Service in Windows Service Control Manager. Common root causes include the following:

* The Azure AD Connect sync service account, which is used by the Synchronization Service as its security context, has its password changed recently. To resolve this issue, refer to article [Changing the Azure AD Connect sync service account password](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-change-serviceacct-pass).
* The Azure AD Connect sync service account is not granted **Logon as a Service** right. For more information on how to grant this right, refer to article [Log on as a service](https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/log-on-as-a-service).
* The Azure AD Connect server is using **LocalDB** as its database, which has a 10-GB limit. When using LocalDB and this limit is reached, the Synchronization Service can no longer start or synchronize properly. To recover from this issue, follow the steps described in article [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-recover-from-localdb-10gb-limit).

## **Recommended Documents**

* [Changing the Azure AD Connect sync service account password](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-change-serviceacct-pass)  
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-recover-from-localdb-10gb-limit)  
