<properties
    pageTitle="Password synchronization does not work – No passwords are synchronized"
    description="Password synchronization does not work – No passwords are synchronized"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="billmath"
    displayOrder="1221"
    selfHelpType="resource"
    supportTopicIds="32596863"
    resourceTags="directory_ad_connect"
    productPesIds="14785,16579"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="7183c039-47a0-432a-95ef-272beead8260"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Password synchronization does not work – No passwords are synchronized

## **Recommended steps**

**Password synchronization does not work – No passwords synchronized**

Common root causes include:

  * The Active Directory account used by Azure AD Connect to communicate with on-premises Active Directory is not granted **Replicate Directory Changes** and **Replicate Directory Changes All** permissions, which are required for password synchronization.

  * Password synchronization is disabled after an administrator changed the User Sign-In method from **Password Synchronization** to another option such as **Federation with AD FS** in the Azure AD Connect wizard.

  * There is connectivity issue with on-premises Active Directory. For example, some domain controllers are not accessible by Azure AD Connect or [ports required](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-ports#table-1---azure-ad-connect-and-on-premises-ad) are blocked by Firewall.

  * The Azure AD Connect server is currently in staging mode.


To troubleshoot the issue, follow the steps described in section [Troubleshoot password synchronization with Azure AD Connect sync - No passwords are synchronized](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization#no-passwords-are-synchronized-troubleshoot-by-using-the-troubleshooting-task).


**Password synchronization does not work for specific user**

Common root causes include:

  * The on-premises Active Directory User object is enabled for **User must change password at next logon** option. When this option is enabled, the user is assigned a temporary password and will be prompted to change the password on next logon. Azure AD Connect does not synchronize temporary passwords to Azure AD. To resolve this issue, either:

    * Ask the user to sign in to on-premises application (E.g., Windows Desktop) and change the password. The new password will be synchronized to Azure AD, or

    * Have an administrator update the user’s password without enabling the option “User must change password at next logon” option and share the new password with the user.

  * The on-premises Active Directory User object is not correctly configured for object synchronization or password synchronization.

To troubleshoot the issue, follow the steps described in the article [Troubleshoot password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization).