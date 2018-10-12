<properties
    pageTitle="I'm having a problem with self-service password reset"
    description="Password Management/Self-service password change/reset"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045826"
    resourceTags=""
    productPesIds="14785,16579"
    cloudEnvironments="public"
    />

# I'm having a problem with self-service password reset

## **Recommended steps**

**I'm having trouble configuring password reset**

* To learn how to configure password reset for your organization, review this article: [Quick Start: Azure AD self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* Make sure you that you understand the licensing requirements:
  * You must have at least one license assigned in your organization
    * **Cloud only users** - Any Office 365 (O365) paid SKU, or Azure AD Basic
    * **Cloud and/or on-premises users** - Azure AD Premium P1 or P2, Enterprise Mobility + Security (EMS), or Secure Productive Enterprise (SPE)
    * To read more about licensing requirements see the article [Licensing requirements for Azure AD self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)
* If you have a question about self-service password reset, review this article: [Password management frequently asked questions](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-passwords-faq)

**I'm getting an error message**

Review this article to find common errors and their solutions: [Troubleshoot self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-passwords-troubleshoot)

**I'm having a problem with my password reset policy**

* If your password reset policy is not behaving as expected, or if you have questions about password reset policies, review this article: [Password policies and restrictions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy)
* Password reset policies **do not** apply to administrators. Microsoft enforces a strong default two-gate password reset policy for any Azure administrator role. Make sure that you are testing with a user who is not an administrator. For more information on the administrator reset policy, see this article: [Administrator reset policy differences](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#administrator-reset-policy-differences)

**I don't want my users to register additional security info for password reset**

* You can pre-populate data (email and phone attributes) for your users using an API, Powershell, or Azure AD Connect. To learn how read:
  * [Deploying password reset without requiring users to register](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data#set-and-read-authentication-data-using-powershell)
  * [What data is used by password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data)

**I want my users to register their additional security info for password reset**

1. Have your users register their security info for self service password reset by directing them to [aka.ms/ssprsetup](https://account.activedirectory.windowsazure.com/passwordreset/Register.aspx).

2. After data is populated for the user (by the user or by the admin), direct your user to [aka.ms/sspr](https://passwordreset.microsoftonline.com/) so your users can be empowered to reset their own passwords.

3. If users are still experiencing problems they are most likely **federated** or **password hash synched** users. This means there is likely a problem with the Password Writeback service.
* For more information on Password Writeback configuration read:
  * [How to enable users to reset their Azure AD passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
  * [How to enable users to reset or change their on-premises Active Directory passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-or-change-their-ad-passwords)


## **Recommended documents**

* [FAQ - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset)
* [FAQ - Password Reset Registration](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-reset-registration)
* [FAQ - Password Change](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq#password-change)
* [Troubleshoot - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [Troubleshoot - Password Reset Registration](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-registration-portal)
* [How to update your own password](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-update-your-own-password)
* [Getting Started with Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [Best Practices - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)
