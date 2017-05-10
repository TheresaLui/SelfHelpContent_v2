<properties
    pageTitle="I'm having a problem with self-service password reset"
    description="Password Management/Self-service password change/reset"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia, gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045826"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# I'm having a problem with self-service password reset
## **Recommended steps**


**I'm having trouble deploying password reset to my organization**

* Make sure you that you understand the licensing requirements:
  * You must have at least one license assigned in your organization
    * **Cloud only users** - Any Office 365 (O365) paid SKU, or Azure AD Basic
    * **Cloud and/or on-premises users** - Azure AD Premium P1 or P2, Enterprise Mobility + Security (EMS), or Secure Productive Enterprise (SPE)
    * Click [here](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing) to read more about licensing requirements.


* [Quick Start: Azure AD self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)


**I don't want my users to register additional security info for password reset**

* You can pre-populate data (email and phone attributes) for your users using an API, Powershell, or Azure AD Connect. To learn how read:
  * [Deploying password reset without requiring users to register](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data#set-and-read-authentication-data-using-powershell)
  * [What data is used by password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data)




**I want my users to register their additional security info for password reset**

1. Have your users register their security info for self service password reset by directing them to [aka.ms/ssprsetup](https://account.activedirectory.windowsazure.com/passwordreset/Register.aspx).

2. After data is populated for the user (by the user or by the admin), direct your user to [aka.ms/sspr](https://passwordreset.microsoftonline.com/) so your users can be empowered to reset their own passwords.

3. If users are still experiencing problems they are most likely **federated** or **password hash synched** users. This means there is likely a problem with the Password Writeback service.
<!-- this is where "quick writeback fixes was" -->
  * For more information on Password Writeback configuration read:
    * [How to enable users to reset their Azure AD passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
    * [How to enable users to reset or change their on-premises Active Directory passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-or-change-their-ad-passwords)


<!--
Top Tips doc is being worked on - John will publish soon

* For quick writeback fixes check [Tip 5](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-5-writeback---look-at-the-application-event-log-on-your-aad-connect-machine-to-troubleshoot-password-writeback) and [Tip 6](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-6-writeback---ensure-you-enable-the-correct-permissions-firewall-rules-and-connection-settings-for-password-writeback) from our [Top Tips](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)

-->






## **Recommended documents**
<!--
 John Flores is working on a new version of this doc. Once that is live will reactivate/update link

 * [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin) -->
* [FAQ - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset)
* [FAQ - Password Reset Registration](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset-registration)
* [FAQ - Password Change](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-change)
* [Troubleshoot - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [Troubleshoot - Password Reset Registration](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-registration-portal)
* [How to update your own password](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-update-your-own-password)
* [Getting Started with Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [Best Practices - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)
