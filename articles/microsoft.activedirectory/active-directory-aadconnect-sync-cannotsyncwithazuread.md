<properties
    pageTitle="Synchronization Service cannot import/export changes from Azure AD"
    description="Synchronization Service cannot import/export changes from Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder=""
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Synchronization Service cannot import/export changes from Azure AD

## **Recommended steps**
Common root causes include the following:

* The Azure AD service account, which is used by the Synchronization Service to communicate with Azure AD, is either deleted, has its password changed or has its userPrincipalName changed. To resolve this issue, refer to article [Azure AD Connect sync: How to manage the Azure AD service account](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass).

* There is network connectivity issue between the Azure AD Connect server and Azure AD. To troubleshoot connectivity issue, refer to article [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity).

## **Recommended documents**
* [Azure AD Connect sync: How to manage the Azure AD service account](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)  
* [Troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-connectivity)  
