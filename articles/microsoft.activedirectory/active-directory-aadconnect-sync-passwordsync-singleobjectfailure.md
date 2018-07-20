<properties
    pageTitle="Password synchronization does not work for specific user"
    description="Password synchronization does not work for specific user"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="billmath"
    displayOrder="1221"
    selfHelpType="resource"
    supportTopicIds="32596863"
    resourceTags="directory_ad_connect"
    productPesIds="14785"
    cloudEnvironments="public"
/>

# Password synchronization does not work for specific user

## **Recommended steps**
Common root causes include:

* The on-premises Active Directory User object is enabled for **User must change password at next logon** option. When this option is enabled, the user is assigned a temporary password and will be prompted to change the password on next logon. Azure AD Connect does not synchronize temporary passwords to Azure AD. To resolve this issue, either:
  * Ask the user to sign in to on-premises application (E.g., Windows Desktop) and change the password. The new password will be synchronized to Azure AD, or
  * Have an administrator update the user’s password without enabling the option “User must change password at next logon” option and share the new password with the user.

* The on-premises Active Directory User object is not correctly configured for object synchronization or password synchronization. To troubleshoot the issue, follow the steps described in the article section [Troubleshoot password synchronization with Azure AD Connect sync - One object is not synchronizing passwords](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization#one-object-is-not-synchronizing-passwords).


## **Recommended documents**
* [Implement password synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization)  
* [Troubleshoot password synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-synchronization)  
