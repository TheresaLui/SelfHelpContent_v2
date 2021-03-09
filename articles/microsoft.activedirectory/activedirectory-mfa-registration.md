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

### Resolve problems with the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)

You can quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom):  
 
1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request ID, or correlation ID.
3. Review the diagnostic results that show the details of what happened and what actions you can take to make changes, if any changes are needed.
   
## **Recommended Steps**
 
Check the scenario that is applicable:

1. If registration is completed, but an error message is received while signing in:
    * Check the [sign-in logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/SignIns: see if any error code generated for e.g. 50076. Search the error code in below URL: https://login.microsoftonline.com/error and follow the presented troubleshooting steps 
 
2: If you are looking for combined registration(MFA+SSPR) or experiencing issues while performing combined registration, go to [Manage user feature preview settings](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/UserSettings), and follow the instructions on [how to enable combined security information registration in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/howto-registration-mfa-sspr-combined?WT.mc_id=Portal-Microsoft_Azure_Support)
 
3. If you've selected any of the following MFA registration methods and are receiving error messages:
    a. Authenticator app
    	* [FAQ about the Microsoft Authenticator app](https://docs.microsoft.com/azure/active-directory/user-help/user-help-auth-app-faq)
	* [Issues with Microsoft Authenticator not displaying Approval message](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/issues-with-microsoft-authenticator-not-popping-up-approval/m-p/267794)
    b. Phone or SMS: [Common problems with two-factor verification and your work or school accounts](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-troubleshoot)
 
4. If you want to change the verification method, go to the [MyApps website](https://myapps.microsoft.com) and select the verification method you want, and follow the steps to [Change your two-factor verification method and settings](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-manage-settings) 
