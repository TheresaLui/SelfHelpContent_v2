<properties
    pageTitle="Synchronization Service cannot import/export changes from on-premises AD"
    description="Synchronization Service cannot import/export changes from on-premises AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="57"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="5ff2b37b-4313-42db-b9f0-2a0fc89172c6"
/>

# Synchronization Service cannot import/export changes from on-premises AD

## **Recommended steps**

Common root causes include the following:

* The AD DS account, which is used by the Synchronization Service to communicate with on-premises AD, is either deleted, has its password changed or has its userPrincipalName changed. To resolve this issue, refer to article [Changing the AD DS account password](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-change-addsacct-pass).

* There is network connectivity issue between the Azure AD Connect server and Azure AD. To troubleshoot connectivity issue, refer to article [Troubleshoot connectivity issues with Azure AD Connect](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-connectivity).

## **Recommended documents**

* [Changing the AD DS account password](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-change-addsacct-pass)   
* [Troubleshoot connectivity issues with Azure AD Connect](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-connectivity)  
