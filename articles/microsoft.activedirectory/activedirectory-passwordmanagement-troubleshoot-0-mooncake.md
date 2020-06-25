<properties
    pageTitle="Problems with licensing"
    description="Top Tips from customers - Tip 1"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    ms.author="gahug"
    displayOrder="24"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="MoonCake"
    articleId="activedirectory-passwordmanagement-troubleshoot-0-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Problems with licensing

## **Recommended Steps**

**I don't understand the licensing requirements**

* Make sure you have a [valid license](https://www.azure.cn/pricing/details/active-directory/) for Azure AD Password Reset.

* Azure AD password reset is available in 3 tiers:

  * Azure AD Free - cloud administrations can reset their own passwords
  * Azure AD Basic or any Paid O365 Subscription - cloud users and cloud administrators can reset their own passwords
  * Azure AD Premium - any user or administrator (cloud, federated, password hash synced users) can reset passwords. Password writeback must be enabled to support some scenarios.

* Premium features are also included in:

    * Enterprise Mobility + Security E3
    * Enterprise Mobility + Security E5
    * Secure Productive Enterprise E3
    * Secure Productive Enterprise E5
