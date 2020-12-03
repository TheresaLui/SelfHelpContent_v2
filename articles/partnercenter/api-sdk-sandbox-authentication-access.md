<properties
	pageTitle="CSP APIs, SDK, sandbox - API authentication or access issues"
	description="CSP APIs, SDK, sandbox - API authentication or access issues"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="brentserbus"
	ms.author="brserbus"
	displayOrder=""
	articleId="api_sdk_sandbox_authentication_access"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32725822"
	clientIds='partnercenter'
	resourceTags="csp"
	productPesIds="17002"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_API_and_Integration_Support"
/>

# API authentication or access issues

## **Recommended Steps**

To help you integrate and test your API integration, Partner Center supports the creation of an [integration sandbox account](https://docs.microsoft.com/partner-center/develop/set-up-api-access-in-partner-center#integration-sandbox-account).

By default, there is no integration sandbox account. You must [create one](https://docs.microsoft.com/partner-center/develop/set-up-api-access-in-partner-center#create-an-integration-sandbox) yourself from [here](https://partner.microsoft.com/pcv/enrollment/sandbox) if you plan to use the Partner Center SDK. Requirements for API integration and sandbox account access:
- Your CSP tenant must be either an Indirect provider or a Direct bill partner
- Indirect resellers, Advisors and MPN Partners tenants do not support API integration
- You can enroll as Direct Bill Partner after fulfilling CSP Direct requirements. Minimum requirements are [here](https://docs.microsoft.com/partner-center/direct-partner-new-requirements#minimum-requirements).

After your account is set up, you must [enable API access](https://docs.microsoft.com/partner-center/develop/set-up-api-access-in-partner-center#enable-api-access) before you can use the Partner Center SDK with the integration sandbox. You need to enable access to the API separately for both your primary Partner account and your integration sandbox account.

## **Recommended Documents**

* [Set up API access in Partner Center](https://docs.microsoft.com/partner-center/develop/set-up-api-access-in-partner-center) 
* [Partner Center authentication](https://docs.microsoft.com/partner-center/develop/partner-center-authentication)
* [Integration sandbox account](https://docs.microsoft.com/partner-center/develop/set-up-api-access-in-partner-center#integration-sandbox-account)
	 
