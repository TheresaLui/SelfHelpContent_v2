<properties
	pageTitle="Configure a new NPS extension deployment"
	description="Covers problems during initial setup and configuration of the NPS extension"
	infoBubbleText="Configure a new NPS extension deployment"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="InbarckMS"
	ms.author="inbarc"
	displayOrder="5"
	articleId="4a829bb2-a970-4a89-90bb-efea718df9fe"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32615400"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Configure a new NPS extension deployment

## **Recommended Steps**

1. Would you like to enforce MFA on you VPN? Today, many VPN vendors supports SAML authentication. If your VPN supports SAML authentication – you can either look for them in the Enterprise Applications App Gallery or you can add a custom SAML app. Once the VPN is federated with Azure AD, you can protect it by requiring MFA or trusted device, like any other Conditional Access policy. See more information about integrating  SAML apps in Azure AD here:  [SAML SSO](https://docs.microsoft.com/azure/active-directory/manage-apps/what-is-single-sign-on#saml-sso) and deploying MFA using a [Conditional Access policy](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#create-conditional-access-policy).

2. If your VPN doesn’t support SAML authentication, you can protect RADIUS authentication with MFA using the [Azure MFA NPS extension](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-nps-extension).

## **Recommended Documents**

* [NPS extension prerequisites](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-nps-extension)

* [Integrate your VPN infrastructure with Azure MFA by using the NPS extension](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-nps-extension-vpn)

* [Integrate your Remote Desktop Gateway infrastructure using the NPS extension](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-nps-extension-rdg) 

* [Troubleshooting the NPS extension](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-nps-extension#troubleshooting)