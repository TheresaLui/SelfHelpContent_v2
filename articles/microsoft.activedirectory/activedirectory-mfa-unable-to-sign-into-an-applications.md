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
# Unable to sign in to an application due to MFA


Resolve problems with the Sign-in Diagnostic using the following steps. 
This topic covers issues related to sign-in, account lockout, app passwords, and legacy authentication.

## **Recommended Steps**

**To diagnose problems related to user sign-in:**  
 
1. Launch the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)
2. Find the event you want to analyze by entering details you have about the user, application, time of sign-in, request ID, or correlation ID.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes (if any changes are needed).
   

**To avoid sign-in blocks when using MFA:**

1. Enable modern authentication: If you are getting blocked when trying to access Exchange Online, make sure you have enabled [modern authentication in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online).

2. Use Office and mail clients that support modern authentication: Make sure that your users are not using older clients that don't support modern authentication. [Office 365 Client App Support - Modern Authentication](https://docs.microsoft.com/office365/enterprise/office-365-client-support-modern-authentication).

3. Disable legacy authentication: Are you using Conditional Access to enforce MFA? After you've taken the preceding steps and are using modern authentication successfully, we strongly recommend blocking legacy authentication: [Blocking legacy authentication](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-block-legacy-authentication).

## **Recommended Documents**

* [Create app passwords from the Security info (preview) page](https://docs.microsoft.com/azure/active-directory/user-help/security-info-app-passwords)
* [Enable and use Azure AD Multi-Factor Authentication with legacy applications using app passwords](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-app-passwords)
* [Manage app passwords for two-step verification](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords)
