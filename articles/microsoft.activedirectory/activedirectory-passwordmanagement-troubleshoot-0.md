<properties
    pageTitle="Problems with licensing"
    description="Top Tips from customers - Tip 1"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="100"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="a447252e-69f4-4283-885e-ae2cd1e56715"
	ownershipId="AzureIdentity_User"
/>

# Problems with licensing

## **Recommended steps**
**I don't understand the licensing requirements**
* Make sure you have a [valid license](https://azure.microsoft.com/pricing/details/active-directory/) for Azure AD Password Reset.

* Azure AD password reset is available in 3 tiers:
  * Azure AD Free - cloud administrations can reset their own passwords
  * Azure AD Basic or any Paid O365 Subscription - cloud users and cloud administrators can reset their own passwords
  * Azure AD Premium - any user or administrator (cloud, federated, password hash synced users) can reset passwords. Password writeback must be enabled to support some scenarios.


*  Premium features are also included in:
    * Enterprise Mobility + Security E3
    * Enterprise Mobility + Security E5
    * Secure Productive Enterprise E3
    * Secure Productive Enterprise E5



## **Recommended documents**
* [Problems with licensing](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-1-licensing---make-sure-you-understand-the-licensing-requirements)
* [General password reset licensing information](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-customize#what-customization-options-are-available)
* [Per-feature password reset licensing information](https://docs.microsoft.com/azure/active-directory/active-directory-passwords#pricing-and-availability)
* [Scenarios supported for password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#scenarios-supported-for-password-writeback)
* [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
