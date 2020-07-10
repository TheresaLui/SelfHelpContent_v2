<properties
    pageTitle="Password policies"
    description="Password policies"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="sahenry"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615406"
    resourceTags=""
    productPesIds="16579,14785"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="e76b52f3-9670-440f-bad7-e214ee4dbe87"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# I'm having problems with password policies
## **Recommended steps**

**I'm having problems with the password policy for a user**

* The password policy for a user depends on whether the user is cloud only or on-premises.
* Cloud only users must choose a password that meets the requirements in this article: [Password policies that only apply to cloud user accounts](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#password-policies-that-only-apply-to-cloud-user-accounts)
* On-premises users must choose a password that meets the on-premises requirements. If an on-premises user is unable to set their password, check your on-premises requirements.

**I don't know how to set or check password expiration policies**

* You can set and check the expiration policy for cloud users in your tenant by using PowerShell. Follow the instructions in this article: [Set or check the password policies by using PowerShell](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#set-or-check-the-password-policies-by-using-powershell)
* The password expiration policy for on-premises users is set in your on-premises AD. 

## **Recommended documents**
* [Getting Started with Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
* [Troubleshoot Administrator-initiated Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [FAQ - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)
