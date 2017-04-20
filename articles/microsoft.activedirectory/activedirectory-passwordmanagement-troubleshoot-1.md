<properties
    pageTitle="Tip 2: TESTING - Test with an end user, not an administrator, and pilot with a small set of users"
    description="Top Tips from customers - Tip 2"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    displayOrder="200"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="public"
 />
# Tip 2: TESTING
## Test with an end user, not an administrator, and pilot with a small set of users
When you test with an administrator, we enforce the administrator password reset policy, which is defined below.  This means that you will NOT see the expected results of the policy you have configured for your end users.

The policies configured in the administrative UX ONLY apply to end-users, not, administrators. Microsoft enforces strong default password reset policies for your administrators - which may be different than the policies you set for your end-users - in order to ensure your organization stays secure.

### Administrator password reset policy
* **Applies to** - any administrator role (Global Administrator, Helpdesk Administrator, Password Administrator, etc.)
* **One gate policy applies...**
 * ...for first 30 days after a trial is started created **OR**
 * ...when a vanity domain is not present **AND** Azure AD Connect is not syncing identities
 * **_Requires_**: any **one** of Authentication Email, Alternate Email, Authentication Phone, Mobile Phone, or Office Phone to have a value present
* **Two gate policy applies...**
 * ...after the first 30 days of a trial has passed **OR**
 * ...when a vanity domain is present **OR**
 * ... you have enabled Azure AD Connect to synchronize identities from your on-premises environment
 * _**Requires**_: any **two** of Authentication Email, Alternate Email, Authentication Phone, Mobile Phone, or Office Phone to have a value present





[view on DOCS.com](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#tip-2-testing---test-with-an-end-user-not-an-administrator-and-pilot-with-a-small-set-of-users)

## **Recommended documents**

* [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin)
* [Getting Started with Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
* [FAQ - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [Troubleshoot - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot)
