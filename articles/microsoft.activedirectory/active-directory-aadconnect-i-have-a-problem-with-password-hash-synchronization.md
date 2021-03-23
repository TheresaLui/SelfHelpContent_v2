<properties
    pageTitle="I have a problem with Password Hash Synchronization"
    description="I have a problem with Password Hash Synchronization"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32684516"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="b256c701-58a4-42b5-b18c-2ed31cbeae2a"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# I have a problem with Password Hash Synchronization

## **Recommended Steps**

### Password Hash Synchronization doesn't work at all

When Password Hash Synchronization doesn't work, this results in some of the following common issues:

* The Active Directory account used by Azure AD Connect to communicate with on-premises Active Directory is not granted **Replicate Directory Changes** and **Replicate Directory Changes All** permissions, which are required for password synchronization. You need to fix this by granting these permissions to the Active Directory account.
* Password hash synchronization is disabled after an administrator changed the User Sign-In method from **Password Synchronization** to another option, such as **Federation with AD FS** in the Azure AD Connect wizard. You can fix this by re-enabling the password hash synchronization feature in the Azure AD Connect wizard.
* There is a **connectivity issue** with on-premises Active Directory. For example, some domain controllers are not accessible by Azure AD Connect or [ports required](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-ports#table-1---azure-ad-connect-and-on-premises-ad) are blocked by Firewall. To fix or mitigate the issue, make sure that the connectivity between the Azure AD Connect server and the on-premises Active Directory works correctly.
* The Azure AD Connect server is **currently in staging mode**. If the Azure AD Connect server is in staging mode, it won't not synchronize the password hashes.

To troubleshoot the issue, follow the steps described in section [Troubleshoot password synchronization with Azure AD Connect sync - No passwords are synchronized](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization#no-passwords-are-synchronized-troubleshoot-by-using-the-troubleshooting-task).

### Password Hash Synchronization doesn't work for some of my users

If a password hash isn't syncing for a user, use the troubleshooting task in the **Azure AD Connect** to investigate and resolve the issue:

* [Run the troubleshooting task in the wizard](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync#troubleshooting-task)
* [Use the troubleshooting cmdlet to investigate the password hash syncing issue for a specific user](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization#one-object-is-not-synchronizing-passwords-troubleshoot-by-using-the-troubleshooting-task)

* The on-premises Active Directory User object is enabled for **User must change password at next logon** option. When this option is enabled, the user is assigned a temporary password and will be prompted to change the password on next logon. Azure AD Connect does not synchronize temporary passwords to Azure AD. To resolve this issue, you can do take one of the two following actions:

    * Ask the user to sign in to on-premises application (for example, Windows Desktop) and change the password. The new password will be synchronized to Azure AD
    * Have an administrator update the user's password **without** enabling the option, "User must change password at next logon," and share the new password with the user

* The on-premises Active Directory User object is **not correctly configured** for object synchronization or password synchronization
To troubleshoot this issue, follow the steps for [troubleshooting password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization).

## **Recommended Documents**

* [Troubleshoot password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization)
* [What is password hash synchronization?](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-phs)
* [How password hash synchronization works](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization#how-password-hash-synchronization-works)
* [Deploy password hash synchronization](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization#enable-password-hash-synchronization)
* I've already configured password hash synchronization, but...
    * [Password hash synchronization doesn't work for any of my users](password-hash-synchronization-does-not-work-at-all)
    * [Password hash synchronization works for some users, but not all](password-hash-synchronization-does-not-work-for-some-of-my-users)
    * [Password hash synchronization fails after Azure AD Connect is installed on a Windows Server 2019-based server](https://docs.microsoft.com/troubleshoot/azure/active-directory/tvp-errors-when-aadconnect-installed-on-windows-server-2019)
