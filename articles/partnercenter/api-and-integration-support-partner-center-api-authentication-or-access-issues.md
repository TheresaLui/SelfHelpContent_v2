<properties
	pageTitle="Partner Center API and Integration Support Partner Center API authentication or access issues"
	description="Partner Center API and Integration Support Partner Center API authentication or access issues"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="MiaZhu-cn"
	ms.author="v-miazhu"
	displayOrder=""
	articleId="partnercenter_api_and_integration_support_partner_center_api_authentication_or_access_issues"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32692591"
	clientIds="partnercenter"
	resourceTags="csp"
	productPesIds="17002"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_API_and_Integration_Support"
/>

# Partner Center API and Integration Support Partner Center API authentication or access issues

## **Recommended Steps**

* All partners direct bill, indirect partners and CPV’s should follow [partner security requirements](https://docs.microsoft.com/partner-center/partner-security-requirements)
* CPVs
  * A CPV is an independent software vendor that develops apps for use by CSP partners to integrate with Partner Center APIs.
  * A CPV isn't a CSP partner with direct access to the Partner Center dashboard or APIs.
  * [CPV Overview Document](https://assetsprod.microsoft.com/cpv-partner-application-overview.pdf)
* CSP indirect providers and CSP direct partners who are using app ID + user authentication and directly integrate with Partner Center APIs
  * [CSP Overview Document](https://assetsprod.microsoft.com/csp-partner-application-overview.pdf)
  * Refer to [Partner Center Authentication](https://docs.microsoft.com/partner-center/develop/partner-center-authentication). Partner Center uses Azure Active Directory for authentication. When interacting with the Partner Center API, SDK, or PowerShell module you must correctly configure an Azure AD application and then request an access token.
  * API Access for Partner account and Sandbox Account refer [Partner Account and Integration Sandbox API Access](https://docs.microsoft.com/partner-center/develop/set-up-api-access-in-partner-center)
  * Secure Application Model  .NET - [Sample Code](https://docs.microsoft.com/partner-center/develop/console-test-app)
  * [Additional Developer Documentation](https://docs.microsoft.com/partner-center/develop/)

**Guidelines for Partner Center API/SDK Onboarding**

* Create and register an [application](https://docs.microsoft.com/partner-center/develop/enable-secure-app-model#create-a-web-app)  
* Get an [Authorization Code](https://docs.microsoft.com/partner-center/develop/enable-secure-app-model#get-authorization-code)
* Get an [Access Token](https://docs.microsoft.com/partner-center/develop/enable-secure-app-model#get-access-token)
The access token is used for the authentication and refresh token to get the new access token. [Get a Refresh Token](https://docs.microsoft.com/partner-center/develop/enable-secure-app-model#get-refresh-token)
* [Make a Partner Center API call](https://docs.microsoft.com/partner-center/develop/enable-secure-app-model#make-partner-center-api-calls)
* The validity of the access token is 60 mins while for refresh token is 90 days. If you want to prevent the refresh token from expiry, perform periodic update of the new refresh token at the time of each new authentication request.  
* The refresh token must be [stored as a secret](https://docs.microsoft.com/rest/api/keyvault/setsecret/setsecret) in Key Vault.
* The reply URLs should be set properly as per your application.
  * If partners are testing their custom code or [.Net samples](https://github.com/microsoft/Partner-Center-DotNet-Samples/tree/master/secure-app-model) for Secure App Model then please refer [create application](https://docs.microsoft.com/partner-center/develop/enable-secure-app-model#create-a-web-app) and follow the instructions on how to create the web app.
  * If Partners are testing [.Net SDKSamples](https://github.com/microsoft/Partner-Center-DotNet-Samples/tree/master/sdk) or Partner Center PowerShell then reply URL has to be set as – "urn:ietf:wg:oauth:2.0:oob". Refer to [Azure AD application](https://docs.microsoft.com/powershell/partnercenter/secure-app-model?view=partnercenterps-1.5#azure-ad-application) for more details.
* Application secret should be up to date.
