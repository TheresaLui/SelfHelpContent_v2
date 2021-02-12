<properties
    pageTitle="Synchronizing AD to Azure AD/Password synchronization"
    description="Synchronizing AD to Azure AD/Password synchronization"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32142240"
    resourceTags=""
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="a2c07ff1-f903-4199-9f92-8cad5067a668"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Synchronizing AD to Azure AD/Password synchronization

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

To troubleshoot the issue, follow the steps described in the article section [Troubleshoot password synchronization with Azure AD Connect sync - One object is not synchronizing passwords](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization#one-object-is-not-synchronizing-passwords-troubleshoot-by-using-the-troubleshooting-task).
