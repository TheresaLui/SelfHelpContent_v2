<properties
    pageTitle="Problems testing password reset policy"
    description="Top Tips from customers - Tip 2"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    ms.author="gahug"
    displayOrder="23"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="MoonCake"
	articleId="activedirectory-passwordmanagement-troubleshoot-1-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Problems testing password reset policy

## **Recommended Steps**

**I reset my password but it used a different policy from the one I set in the portal**

* Test with an end-user not an administrator.

* When you test with an administrator, we enforce the administrator password reset policy (defined below). This means that if you test with an administrator you won't see the policy you configured in through the Azure portal.

* The policies configured in the Azure portal only apply to end users.
* Microsoft enforces stronger default password reset policies for your administrators (which might be different than the policies you set for your end-users) in order to ensure that your organization is more secure.

**I want to understand the administrator password reset policy**

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
