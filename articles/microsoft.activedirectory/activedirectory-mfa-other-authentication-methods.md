<properties
	pageTitle="Authentication methods - Other (tokens, 3rd party)"
	description="Cover problems related to other authentication methods like problems with creating hardware OATH tokens in Azure AD and 3rd party MFA providers"
	infoBubbleText="Authenticator App"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="InbarckMS"
	ms.author="inbarc"
	displayOrder="4"
	articleId="0b08f3e1-f90a-48f1-af92-442f5f55288e"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739613"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Authentication methods - Other (tokens, 3rd party)

## **Recommended Steps**  

You can quickly determine the issue or diagnose issues related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom):

1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request ID, or correlation ID.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes, if any changes are needed.
   
## **Recommended Documents**

* [Create app passwords from the Security info (preview) page](https://docs.microsoft.com/azure/active-directory/user-help/security-info-app-passwords)
* [Enable and use Azure AD Multi-Factor Authentication with legacy applications using app passwords](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-app-passwords)
* [Manage app passwords for two-step verification](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords)
* [Hardware OATH tokens](https://docs.microsoft.com/azure/active-directory/authentication/concept-authentication-methods#oath-hardware-tokens-public-preview)
* Third-party MFA providers: [Custom Controls](https://docs.microsoft.com/azure/active-directory/conditional-access/controls)
