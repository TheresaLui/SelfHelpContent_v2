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
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Streaming endpoint performance guidance
<!--issueDescription-->
Our internal service telemetry detected that the customer's streaming endpoint(s) under the Azure Media Services account **<!--$amsAccountName--> amsAccountName <!--/$amsAccountName-->** had performance issues from  **<!--$startTime--> startTime <!--/$startTime-->** to **<!--$endTime--> endTime <!--/$endTime-->** (UTC) due to high traffic or heavy processing.
<!--/issueDescription-->

**Standard Streaming Endpoint**

A Standard Streaming Endpoint is suitable for most streaming workloads, and it is able to auto scale automatically when outbound bandwidth increases. However, the auto scale may not react fast enough if the speed of workload increases rapidly. This could cause the 503 status code (Service Unavailable) or 500 status code (Internal Server Error) with TIMEOUT error to be returned by the streaming endpoint(s).

**Premium Streaming Endpoint**

A Premium Streaming Endpoint is recommended for professional usage. It provides 200-Mbps bandwidth per streaming unit, the customer controls the number of streaming units they use. The current streaming units may not be enough to deal with large volume of workload. The 503 status code (Service Unavailable) or 500 status code (Internal Server Error) with TIMEOUT error  could be returned by the streaming endpoint(s).


## **Recommended Steps**

**Standard Streaming Endpoint**

Check if CDN is enabled. If not, enable CDN. If enabled already, enable origin shield and request consolidation at CDN. If changing the CDN configuration doesn't help, the customer should move to the premium streaming endpoint.

**Premium Streaming Endpoint**

Check if CDN is enabled. If not, enable CDN. If enabled already, enable origin shield and request consolidation at CDN. If changing the CDN configuration doesn't help, the customer should increase streaming units based on the bandwidth usage data. 

It is also possible that the customer is streaming too many assets at the same time on the same streaming endpoint. It will help the playback experience if the customer distributes the assets into different streaming endpoints.

The customer should monitor their streaming bandwidth with Azure Monitor, and increase the number of streaming units for every 200-Mbps traffic they expect to serve. For more information, see these articles:

- [Monitor Media Services metrics](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-howto)
- [Streaming Endpoint metrics](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-diagnostic-logs#streaming-endpoint)

## **Recommended Documents**

* [Azure Media Services v3 quotas and limitations](https://docs.microsoft.com/azure/media-services/latest/limits-quotas-constraints)
* [Streaming Endpoints concept](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept)
* [Working with CDN](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept#working-with-cdn)
* [Azure CDN](https://docs.microsoft.com/azure/cdn/cdn-overview)
