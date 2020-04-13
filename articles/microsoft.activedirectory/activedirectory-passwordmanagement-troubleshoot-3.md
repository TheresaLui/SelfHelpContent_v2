<properties
    pageTitle="Problems with temporary passwords"
    description="Top Tips from customers - Tip 4"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="400"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="d51b7536-ae48-4a80-993b-ca27f3b8ec9f"
	ownershipId="AzureIdentity_User"
/>

# Problems with temporary passwords

## **Recommended steps**
**I don't want to communicate temporary passwords to users**

Once you pre-configure your users for password reset, imagine a scenario where an employee joins your company for the first time. Instead of communicating the temporary password to him or her, you can now just have them navigate to the [Azure AD Password Reset Portal](https://passwordreset.microsoftonline.com) to reset their passwords.

If the user is using a [Windows 10 Azure AD Domain-joined device](https://docs.microsoft.com/azure/active-directory/active-directory-azureadjoin-devices-group-policy), they can even do this right from the Windows 10 Out of Box sign in screen, allowing them to get access to a brand-new PC without you needing to lift a finger :).

To learn how to do this using an API, PowerShell, or Azure AD Connect, take a read of the documentation below. Once you pre-populate this data, just send your users to reset their passwords, and they can get into their accounts right away:
* [Deploying password reset without requiring users to register](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
* [What data is used by password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)






## **Recommended documents**
* [Avoid temporary passwords](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-4-deployment---use-password-reset-to-obviate-the-need-to-communicate-temporary-passwords)
* [Deploying password reset without requiring users to register](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
* [What data is used by password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)
* [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [FAQ - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [Troubleshoot - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)
