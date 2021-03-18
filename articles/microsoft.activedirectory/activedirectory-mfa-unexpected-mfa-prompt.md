<properties
	pageTitle="Unexpected MFA prompt"
	description="Cover problems related to MFA prompts and re-authentication requests"
	infoBubbleText="Unexpected MFA prompt"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="InbarckMS"
	ms.author="inbarc"
	displayOrder="10"
	articleId="d454a9dd-8a0c-42d7-9ec3-5026459da6ca"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739621"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Unexpected MFA prompt

### Resolve problems with the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom)

You can quickly find out what happened or diagnose problems related to user sign-in by using the [Sign-in Diagnostic](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/diagnose/symptomId/ms_aad_dxp_signin_caDiagnoseAndSolveSummarySymptom):  
 
1. Launch the Sign-in Diagnostic.
2. Find the event to analyze by entering in the details you have about the user, application, time of sign-in, request Id, or correlation Id.
3. Review the diagnostic results showing the details of what happened and what actions you can take to make changes, if any changes are needed.

## **Recommended Steps**

While many organizations are quickly enabling their workforce to securely work remotely, there are some key steps that can help improve the experience for their users if they are working in a new way:

1. Enable SSO-on devices to reduce authentication prompt for users. By enabling the usage of SSO across applications integrated in Azure AD, the users will have fewer prompts for MFA, and admins can include device state controls for seamless secure access.

	For Windows 10, SSO is enabled when the machine is [Azure AD Joined](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join) or [Hybrid Azure AD Joined](https://docs.microsoft.com/azure/active-directory/devices/concept-azure-ad-join-hybrid).

	For mobile IOS/Android devices,  install the Microsoft Authenticator mobile app.

2. If you allow your users to connect from their personal machines, which are not Azure AD Joined or Hybrid Azure AD Joined:
	Consider extending their [sign-in frequency and configure persistence browser sessions](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime), in order prompt your users less frequently for authentication and MFA.
	
	If you are not using Conditional Access, you can reduce authentication prompts by enabling [Keep me signed-in](https://docs.microsoft.com/azure/active-directory/fundamentals/customize-branding) under your tenant branding.

3. Install the [Microsoft Authenticator mobile application](https://docs.microsoft.com/azure/active-directory/user-help/user-help-auth-app-faq) on mobile devices. The Authenticator app is more than just MFA, because it functions as a token broker for all other Microsoft apps on the device, which reduce MFA prompts.

4. Review and update [Azure AD named locations](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-configure-named-locations). Organizations may be adding capacity for their internet access points for VPNs as their organization enables a remote workforce, so we want to make sure this is accounted for in terms of Conditional Access policies.

## **Recommended Documents**

* [Sign-in frequency and authentication prompts](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
* [Remember MFA on a device](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-mfasettings)
* [End user troubleshooting](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-troubleshoot)
