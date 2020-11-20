<properties
	pageTitle="Authentication methods - Authenticator App"
	description="Covers problems related to the Microsoft Authenticator app like activation and receiving push notification"
	infoBubbleText="Authenticator App"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="InbarckMS"
	ms.author="inbarc"
	displayOrder="2"
	articleId="00962e01-0336-44db-b952-0c2053334a1d"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32615519"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Authentication methods - Authenticator App

**Resolve problems with the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)**
Quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom).  
Steps to use the diagnostic: 
1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request Id, or correlation Id.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes (if any changes are needed).
   
## **Recommended Steps**

1. If a user is not getting a push notification in the Microsoft Authenticator app, please verify they are not shown under the MFA blocked users as described here: [Block and unblock users](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-mfasettings#block-and-unblock-users).

2. If the user is not blocked for MFA but does not receive a push notification, they can open the Microsoft Authenticator app, which will pull the pending approval requests.	

3. The user can also click on **Sign in another way** and choose **use a verification code from my mobile app** as an alternative method to sign-in.

## **Recommended Documents**

* The Microsoft Authenticator App  is the only available method for my users  - [Learn more about security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults).

* [Authenticator App FAQ](https://docs.microsoft.com/azure/active-directory/user-help/user-help-auth-app-faq)

## **Recommended Videos**

* [How to set up Authenticator App on a new phone (2min)](https://youtu.be/jTwtosQkn6I)
