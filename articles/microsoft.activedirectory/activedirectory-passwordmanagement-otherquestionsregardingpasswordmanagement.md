<properties
    pageTitle="Other questions about password reset"
    description="Password reset/Other questions regarding password reset"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zchia"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565599"
    resourceTags=""
    productPesIds="14785,16579"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="a066de9d-2688-40a7-9fd4-b11652a22f38"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# I'm having other problems with password reset

## **Recommended steps**

**I'm having an issue with password reset not covered in the other categories**

* Make sure you are authorized to reset passwords. *Only global, password, and user administrators can reset user passwords.* Global administrators can also reset other privileged administrator's passwords.

* Make sure you that you understand the licensing requirements:
  * You must have at least one license assigned in your organization
    * **Cloud only users** - Any Office 365 (O365) paid SKU, or Azure AD Basic
    * **Cloud and/or on-premises users** - Azure AD Premium P1 or P2, Enterprise Mobility + Security (EMS), or Secure Productive Enterprise (SPE)
    * To read more about licensing requirements see the article [Licensing requirements for Azure AD self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing)

**I'm having problems testing the password reset policy I set**

* Recently applied policies can take several minutes to replicate across all data centers and end-points. Physical distance from the data center will also affect how quickly changes are applied.

* Test with an end user, not an administrator, and pilot with a small set of users. The **policies configured in the Azure portal ONLY apply to end-users, not administrators.** Microsoft enforces a strong default **two gate** password reset policy for any Azure administrator role (Example: Global Administrator, Helpdesk Administrator, Password Administrator, etc.)
   * Learn more about [policies for administrators](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-policy#administrator-password-policy-differences)

**I want to deploy password reset but I don't want to make my users register additional security info**

* Pre-populate data for your users so they don't have to!
   * As an administrator you can set phone and email properties for your users before rolling out password reset to your organization. You can do this using an API, PowerShell, or Azure AD Connect. More information here:
     * [Deploying password reset without requiring users to register](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data#set-and-read-authentication-data-using-powershell)
     * [What data is used by password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-data)

**I'm having problems accessing password reset audit logs**

* Make sure you are authorized to view audit logs. ONLY the following roles are authorized:
  * Global administrator
  * Security administrator
  * Security reader

**I want to see all password reset audit events from the time I initially deployed**

* Up to 120,000 password reset/registration events are stored in the reports from the last 30 days. This maximum applies to the UI when downloading the CSV. 1 million events are available through PowerShell.
* Learn more with the links below:
  * [Self-service password reset events from the Azure AD Reports and Events API](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-retrieve-password-management-events-from-the-azure-ad-reports-and-events-api)
  * [How to download password reset registration events quickly with PowerShell](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-download-password-reset-registration-events-quickly-with-powershell)

**I want to understand more about password reset reporting capabilities**

* See who is registering for or resetting passwords with Azure AD password reset audit logs in the Azure portal under **Users and groups**
  * For more detailed information check out the links that follow:
    * [Password reset reports overview](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#overview-of-password-management-reports)
    * [How to view password reset reports in the Azure portal](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-view-password-management-reports)
    * [Self-service password reset events from the Azure AD Reports and Events API](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-retrieve-password-management-events-from-the-azure-ad-reports-and-events-api)
    * [How to download password reset registration events quickly with PowerShell](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights#how-to-download-password-reset-registration-events-quickly-with-powershell)


## **Recommended documents**

* [FAQ - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [Troubleshoot - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)
* [Getting started - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started)
* [Best Practices - Password Reset ](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-best-practices)
* [Audit logs - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-get-insights)
* [Password policies - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-policy)
* [Learn more - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more)
* [How Password Reset Works](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-how-it-works)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)
