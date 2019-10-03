<properties pageTitle="Streaming endpoint performance guidance"
    description="Solution to streaming endpoint performance issues (status 503)"
    infoBubbleText="See details on the right"
    service="microsoft.media"
    resource="mediaservices"
    authors="Juliako"
    ms.author="juliako"
    displayOrder="1"
    articleId="mediaservices-insights-streamingendpoint-performance"
    diagnosticScenario=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="14885"
    cloudEnvironments="public"
/>

# Streaming endpoint performance guidance

<!--issueDescription-->
**Standard Streaming Endpoint**

A Standard Streaming Endpoint is suitable for most streaming workloads, and it is able to auto scale automatically when outbound bandwidth increases. However, auto scale may not catch up if the speed of workload increases. This could cause status code 503 (Service Unavailable) to be returned by the streaming endpoint.

**Premium Streaming Endpoint**

A Premium Streaming Endpoint is recommended for professional usage. It provides 200-Mbps bandwidth per streaming unit, the customer controls the number of streaming units they use. The current streaming units may not be enough to deal with large volume of workload, a status code 503 (Service Unavailable) could be returned by the streaming endpoint.
<!--/issueDescription-->

## **Recommended Steps**

**Standard Streaming Endpoint**

Check if CDN is enabled. If not, enable CDN. If enabled already, enable origin shield and request consolidation at CDN. If changing the CDN configuration doesn't help, the customer should move to the premium streaming endpoint.

**Premium Streaming Endpoint**

First check if CDN is enabled. If not, enable CDN. If enabled already, enable origin shield and request consolidation at CDN. If changing the CDN configuration doesn't help, the customer should increase streaming units based on the bandwidth usage data. 

It is also possible that the customer is streaming too many assets at the same time on the same streaming endpoint. It will help the playback experience if the customer distributes the assets into different streaming endpoints.

The customer should monitor their streaming bandwidth with Azure Monitor, and increase the number of streaming units for every 200-Mbps traffic they expect to serve. For more information, see these articles:

- [Monitor Media Services metrics](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-howto)
- [Streaming Endpoint metrics](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-diagnostic-logs#streaming-endpoint)

## **Recommended Documents**

* [Azure Media Services v3 quotas and limitations](https://docs.microsoft.com/azure/media-services/latest/limits-quotas-constraints)
* [Streaming Endpoints concept](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept)
* [Working with CDN](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept#working-with-cdn)
* [Azure CDN](https://docs.microsoft.com/azure/cdn/cdn-overview)
