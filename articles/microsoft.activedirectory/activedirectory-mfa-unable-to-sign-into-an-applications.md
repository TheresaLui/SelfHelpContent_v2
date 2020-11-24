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

### Resolve problems with the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)

You can quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom):  
 
1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request Id, or correlation Id.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes (if any changes are needed).
   
# Unable to sign into an applications due to MFA

Covers sign-in problems and account lockout related completing MFA, legacy authentication, or app passwords.

## **Recommended Steps**

To make sure you are not getting blocked from sign-in when using MFA, use the following steps:

1. Enable modern authentication: If you are getting blocked when trying to access Exchange Online, make sure you have enabled [modern authentication in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online).

2. Use Office and mail clients that supports modern authentication: Make sure your users are not using older clients that do not support modern authentication. [Office 365 Client App Support - Modern Authentication](https://docs.microsoft.com/office365/enterprise/office-365-client-support-modern-authentication).

3. Disable legacy authentication: Are you using Conditional Access to enforce MFA? After you've taken the preceding steps and you are using modern authentication successfully, we strongly recommend blocking legacy authentication: [Blocking legacy authentication](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-block-legacy-authentication).
