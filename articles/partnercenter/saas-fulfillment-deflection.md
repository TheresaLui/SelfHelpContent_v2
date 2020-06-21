<properties
	pageTitle="SaaS fullfillment and deployment failures"
	description="Learning more about fulfillment and deployment failures"
	infoBubbleText="Resources to help explain fulfillment for SaaS"
	service="partnercenter"
	resource="marketplace"
	authors="garrett-o"
	ms.author="gaor"
	displayOrder=""
	articleId="marketplace_deploy_failures"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32728236"
	resourceTags="marketplace"
	productPesIds="17006"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Ingestion"
/>

# <-- SaaS deployment deflection -->

If encountering issues with fulfillment of your SaaS offer, the following resources can help identify and address the failure.

## **Recommended Steps**

1. Verify you have registered your SaaS application in the [Azure portal](https://ms.portal.azure.com/) with an [Azure AD application](https://docs.microsoft.com/azure/marketplace/partner-center-portal/pc-saas-registration) to be able to authenticate
2. Confirm you are using the most recent version of the [fulfillment APIs for SaaS offers](https://docs.microsoft.com/azure/marketplace/partner-center-portal/pc-saas-fulfillment-api-v2)
3. Review the expected flows and implementation guidance for [provisioning and how it interacts with your service](https://docs.microsoft.com/azure/marketplace/partner-center-portal/pc-saas-fulfillment-api-v2#provisioning)
4. Verify your implementation handles the expected behavior when calling the [mock API endpoint](https://docs.microsoft.com/azure/marketplace/partner-center-portal/pc-saas-fulfillment-api-v2#mock-apis)
5. Verify when prototyping is complete to change the API version to the production endpoint
6. If still encountering issues or unexpected behavior from the API not covered in the previous resources, file a support ticket outlining the details of your issue for assistance


## **Recommended Documents**

* [SaaS fulfillment APIs](https://docs.microsoft.com/azure/marketplace/partner-center-portal/pc-saas-fulfillment-apis)
* [Register a SaaS application](https://docs.microsoft.com/azure/marketplace/partner-center-portal/pc-saas-registration)
* [SaaS fulfillment APIs, version 2](https://docs.microsoft.com/azure/marketplace/partner-center-portal/pc-saas-fulfillment-api-v2)
* [SaaS fulfillment APIs - FAQ](https://docs.microsoft.com/azure/marketplace/partner-center-portal/saas-fulfillment-apis-faq)
