<properties
    pageTitle="Synchronization Service cannot import/export changes from on-premises AD"
    description="Synchronization Service cannot import/export changes from on-premises AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    ms.author="cychua"
    displayOrder="57"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-aadconnect-sync-cannotsyncwithad-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Synchronization Service cannot import/export changes from on-premises AD

## **Recommended Steps**

Common root causes include the following:

* The AD DS account, which is used by the Synchronization Service to communicate with on-premises AD, is either deleted, has its password changed or has its userPrincipalName changed. To resolve this issue, refer to article [Changing the AD DS account password](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-change-addsacct-pass).

* There is network connectivity issue between the Azure AD Connect server and Azure AD. To troubleshoot connectivity issue, refer to article [Troubleshoot connectivity issues with Azure AD Connect](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-connectivity).

## **Recommended Documents**

* [Changing the AD DS account password](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-change-addsacct-pass)   
* [Troubleshoot connectivity issues with Azure AD Connect](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-connectivity)  
