<properties
    pageTitle="Password synchronization does not work for specific user"
    description="Password synchronization does not work for specific user"
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

# Password synchronization does not work for specific user

## **Recommended steps**
* Common root causes include:

  * The on-premises Active Directory User object is enabled for **User must change password at next logon** option. When this option is enabled, the user is assigned a temporary password and will be prompted to change the password on next logon. Azure AD Connect does not synchronize temporary passwords to Azure AD.

  * The on-premises Active Directory User object is not correctly configured for object synchronization or password synchronization.
  
* To troubleshoot the issue, follow the steps described in section [Troubleshoot password synchronization with Azure AD Connect sync - One object is not synchronizing passwords](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization#one-object-is-not-synchronizing-passwords).


## **Recommended documents**
[Implement password synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization)  
[Troubleshoot password synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization)  
