<properties
    pageTitle="Other questions about password management"
    description="Password Management/Other questions regarding password management"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565599"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# I'm having other problems with password reset

## **Recommended steps**

**Before you start**
* Make sure you have a [valid license](https://azure.microsoft.com/pricing/details/active-directory/) for Azure AD Password Reset.


**I'm having an issue with Password Reset not covered in the other categories**

*  [TESTING](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-2-testing---test-with-an-end-user-not-an-administrator-and-pilot-with-a-small-set-of-users) - Test with an end user, not an administrator, and pilot with a small set of users. The **policies configured in the Azure portal ONLY apply to end-users, not administrators.** Microsoft enforces strong default password reset policies for administrators in order to ensure your organization stays secure.

* [DEPLOYMENT](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-3-deployment---pre-populate-data-for-your-users-so-they-dont-have-to-register) - Pre-populate data for your users so they don't have to!
As an administrator you can set phone and email properties for your users before rolling out password reset to your organization. You can do this using an API, PowerShell, or Azure AD Connect. More information here:
  * [Deploying password reset without requiring users to register](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#deploying-password-reset-without-requiring-end-user-registration)
  * [What data is used by password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#what-data-is-used-by-password-reset)


* [REPORTING](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-7-reporting---see-who-is-registering-or-resetting-passwords-with-the-azure-ad-sspr-audit-logs) - See who is registering or resetting passwords with Azure AD Password Reset Audit Logs in the Azure portal under **Users and groups**
  * For more detailed information check out the links below:
	* [Password management reports overview](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#overview-of-password-management-reports)
	* [How to view password management reports in the Azure portal](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-view-password-management-reports)
	* [Self-service Password Management events from the Azure AD Reports and Events API](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-retrieve-password-management-events-from-the-azure-ad-reports-and-events-api)
	* [How to download password reset registration events quickly with PowerShell](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-download-password-reset-registration-events-quickly-with-powershell)


## **Recommended documents**
* [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [FAQ - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [Troubleshoot - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)
* [Getting started - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [Best Practices - Password Management ](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [Audit logs - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights)
* [Password policies - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-policy)
* [Learn more - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more)
* [How Password Management Works](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-how-it-works)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help)
