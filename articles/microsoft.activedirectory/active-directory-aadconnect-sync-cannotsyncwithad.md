<properties
    pageTitle="Synchronization Service cannot import/export changes from on-premises AD"
    description="Synchronization Service cannot import/export changes from on-premises AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="225"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="5ff2b37b-4313-42db-b9f0-2a0fc89172c6"
	ownershipId="AzureIdentity_User"
/>

# Synchronization Service cannot import/export changes from on-premises AD

## **Recommended steps**
Common root causes include the following:

* The AD DS account, which is used by the Synchronization Service to communicate with on-premises AD, is either deleted, has its password changed or has its userPrincipalName changed. To resolve this issue, refer to article [Changing the AD DS account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-addsacct-pass).

* There is network connectivity issue between the Azure AD Connect server and Azure AD. To troubleshoot connectivity issue, refer to article [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity).

## **Recommended documents**
* [Changing the AD DS account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-addsacct-pass)   
* [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)  
