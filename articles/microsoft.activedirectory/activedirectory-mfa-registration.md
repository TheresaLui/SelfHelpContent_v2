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

- Check if Combined Registration is enabled, if not, enable [Combined Registration](https://docs.microsoft.com/azure/active-directory/authentication/howto-registration-mfa-sspr-combined) 
	- If Combined Registration is enabled: Verify if your tenant's CA policies configured for combined registration are applying by checking the [Azure AD Sign-in Events](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access#azure-ad-sign-in-events)
	- If no Combined Registration CA policies are configured, learn how to [Configure the Azure Multi-Factor Authentication Registration Policy](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy)

- Check [What Authentication and Verification methods are available in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/concept-authentication-methods#how-each-authentication-method-works)
- Follow these steps to register the security methods in the [aka.ms/mysecurityinfo](https://myprofile.microsoft.com)


## **Recommended Videos**

* [Manage security information in My Account (1min)](https://youtu.be/zmC5UzF25Sg)
* [Register and manage your security info (2min)](https://youtu.be/k0oiKQK3LjQ)


## **Recommended Documents**

* [My users can only register the Authenticator App](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) 
* [Azure MFA authentication method analysis](https://docs.microsoft.com/samples/azure-samples/azure-mfa-authentication-method-analysis/azure-mfa-authentication-method-analysis).
* [Conditional Access: Securing security info registration](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-policy-registration)
