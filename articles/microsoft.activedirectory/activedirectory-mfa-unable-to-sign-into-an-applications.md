<properties
	pageTitle="Unable to sign into an applications due to MFA"
	description="Covers sign-in problems and account lockout related completing MFA, legacy authentication or app passwords"
	infoBubbleText="Unable to sign into an applications due to MFA"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="InbarckMS"
	ms.author="inbarc"
	displayOrder="8"
	articleId="953d7345-2034-4074-a224-e0771efebb8a"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739620"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Unable to sign into an applications due to MFA

Covers sign-in problems and account lockout related completing MFA, legacy authentication or app passwords.

## **Recommended Steps**

A few steps to make sure you are not getting blocked from sign-in when using MFA:

1. Enable modern authentication - If you are getting blocked when trying to access Exchange Online, please make sure you have enabled [modern authentication in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online).

2. Use Office and mail clients that supports modern authentication  - please make sure your users are not using older clients that do not support modern authentication. [Office 365 Client App Support - Modern Authentication](https://docs.microsoft.com/office365/enterprise/office-365-client-support-modern-authentication).

3. Disable legacy authentication - Are you using Conditional Access to enforce MFA? Once you have taken the above steps and you are using modern authentication successfully, it is highly recommended to also block legacy authentication: [Blocking legacy authentication](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-block-legacy-authentication).