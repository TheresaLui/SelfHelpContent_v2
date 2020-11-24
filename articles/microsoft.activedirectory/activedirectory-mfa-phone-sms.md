<properties
	pageTitle="Authentication methods - Phone and SMS"
	description="Covers problems related telephony based MFA methods like not receiving text messages or phone calls"
	infoBubbleText="Authenticator App"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="InbarckMS"
	ms.author="inbarc"
	displayOrder="3"
	articleId="40244e3b-206e-430e-ba44-29aea61f32e0"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739614"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Authentication methods - Authenticator App

### Resolve problems with the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)

Quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom).  

1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request Id, or correlation Id.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes, if any changes are needed.

## **Recommended Steps**

If a user is not getting a voice call or SMS,  verify they are not shown under the MFA blocked users: [Block and unblock users](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-mfasettings#block-and-unblock-users).

## **Recommended Documents**

For additional troubleshooting steps for voice and SMS, see [I'm not getting the verification code sent to my mobile device](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-troubleshoot#im-not-getting-the-verification-code-sent-to-my-mobile-device)
