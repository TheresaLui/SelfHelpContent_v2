<properties
	pageTitle="API and Integration Support API Throttling or Rate limits"
	description="API and Integration Support API Throttling or Rate limits"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="felicefan"
	ms.author="v-felice"
	displayOrder=""
	articleId="api_and_integration_support_api_throttling_or_rate_limits"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32781886"
	clientIds='partnercenter'
	resourceTags="csp"
	productPesIds="17002"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_API_and_Integration_Support"
/>

# API and Integration Support - API Throttling or Rate limits

## **Recommended Steps**

When you implement error handling, use the HTTP error code 429 to detect throttling. The failed response includes the Retry-After response header. Backing off requests using the Retry-after delay is the fastest way to recover from throttling.

## **Recommended Documents**

* [API throttling guidance](https://docs.microsoft.com/partner-center/develop/api-throttling-guidance)
