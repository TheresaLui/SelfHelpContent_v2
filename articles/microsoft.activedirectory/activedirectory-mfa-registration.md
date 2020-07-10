<properties
	pageTitle="MFA Registration"
	description="Covers problems related to the MFA registration"
	infoBubbleText="MFA Registration"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="InbarckMS"
	ms.author="inbarc"
	displayOrder="7"
	articleId="5b68c9c8-4dff-4548-aa25-dcc9896848af"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739617"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# MFA Registration

## **Recommended Steps**

As part of your MFA deployment, you will need to make a few decisions about MFA registration. Here are a some best practices and recommendations:

1. If you haven’t enabled the combined security information registration, you can do so by following this document [Combined security information registration](https://docs.microsoft.com/azure/active-directory/authentication/concept-registration-mfa-sspr-combined). This will not only allow you to give the best end user experience, but it will also register your users for Self Service Password Reset (SSPR) as well.

2. If your able to require registration from an Intune compliant device or a Hybrid Azure AD join device, you can setup an additional Conditional Access Policy to require that. See [Conditional Access: Securing security info registration](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-registration).

3. If you can’t require registration to come from a corporate device look to set a specific time period for all users to register by. If they don’t complete by that time frame, block their ability to register and have them contact the help desk to get removed from this block to complete registration. This step helps reduce the chance of an attacker registering for MFA.

4. Have users register and default to the Microsoft Authenticator App as their primary MFA method. This will give you the best end user experience for MFA. You will also get less MFA prompts for the applications on the mobile device.

5. Have users register a backup method. This will help you later when the user gets a new phone and wants to update their number.

6. Run the new MFA Authentication method analyzer when you are done to make sure nothing got missed [Azure MFA authentication method analysis](https://docs.microsoft.com/samples/azure-samples/azure-mfa-authentication-method-analysis/azure-mfa-authentication-method-analysis).

## **Recommended Documents**

* [Identity Protection MFA registration policy](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy)

* [My users can only register the Authenticator App](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)

## **Recommended Videos**

* [Manage security information in My Account (1min)](https://youtu.be/zmC5UzF25Sg)
* [Register and manage your security info (2min)](https://youtu.be/k0oiKQK3LjQ)

