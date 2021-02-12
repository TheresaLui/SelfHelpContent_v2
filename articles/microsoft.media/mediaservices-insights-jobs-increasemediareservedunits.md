<properties
	pageTitle="Increase the number of reserved units"
	description="Advise the customers to increase the number of reserved units"
	infoBubbleText="See details on the right"
	service="microsoft.media"
	resource="mediaservices"
	authors="jinshang"
	ms.author="jinshang"
	displayOrder="1"
	articleId="mediaservices-insights-jobs-increasemediareservedunits"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Increase the number of reserved units

<!--issueDescription-->
Our internal service telemetry detected that your Azure Media Services account **<!--$accountName--> accountName <!--/$accountName-->** has a queue of several jobs, but the account has zero reserved units. Azure Media Services gives you the ability to control how many of your jobs get processed concurrently. If you would like to have better concurrency, you can configure your account to have Media Reserved Units.
<!--/issueDescription-->

## **Recommended Steps**

* To improve concurrency, configure for the number and type of Media Reserved Units via the portal or v2 API

## **Recommended Documents**

* [Scaling Media Processing](https://docs.microsoft.com/azure/media-services/previous/media-services-scale-media-processing-overview)
* [Reserved Unit Type](https://docs.microsoft.com/rest/api/media/operations/encodingreservedunittype)

