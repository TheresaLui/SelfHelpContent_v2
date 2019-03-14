<properties
	pageTitle="Azure Media Services access policy limits and quotas"
	description="Azure Media Services access policy limits and quotas"
	infoBubbleText="Azure Media Services limits and quotas"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-limits-quotas-policies"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632075"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public"
/>

# Azure Media Services access policy limits and quotas

You should try to design a limited set of policies in your Media Services account and reuse them when possible.

In Media Services v3, [Streaming Policies](https://docs.microsoft.com/rest/api/media/streamingpolicies) have a default limit of 100. You should try to reuse them for your [Streaming Locators](https://docs.microsoft.com/rest/api/media/streaminglocators) whenever the same encryption options and protocols are needed.  

In Media Services v2 (legacy), there is a limit of 1,000,000 policies for different policies (for example, for Locator policy or ContentKeyAuthorizationPolicy). You should use the same policy ID if you are always using the same days / access permissions, for example, policies for locators that are intended to remain in place for a long time (non-upload policies).

## **Recommended Documents**

[Azure Media Services v3 quotas and limitations](https://docs.microsoft.com/azure/media-services/latest/limits-quotas-constraints) <br>
[Media Services v2 (legacy) quotas and limitations](https://docs.microsoft.com/azure/media-services/previous/media-services-quotas-and-limitations)
