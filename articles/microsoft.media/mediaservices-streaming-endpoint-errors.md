<properties
	pageTitle="Packaging, origin or streaming endpoint errors"
	description="Packaging, origin or streaming endpoint errors"
	service="microsoft.media"
	resource="mediaservices"
	authors="akucer"
	ms.author="akucer"
	displayOrder="1"
	articleId="mediaservices-streaming-endpoint-errors"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632093"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>
# Packaging, origin or streaming endpoint errors
## **Recommended Documents**
* [Streaming Endpoint (Origin) errors](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes)<br>
	* [400 Bad Request](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#400-bad-request) - The request contains invalid information.<br>
	* [403 Forbidden](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#403-forbidden) - The request is not allowed.<br>
	* [404 Not Found](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#404-not-found) - The operation is attempting to act on a resource that no longer exists.<br>
	* [409 Conflict](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#409-conflict) - The ID provided for a resource on a PUT or POST operation has been taken by an existing resource. Use another ID for the resource to resolve this issue<br>
	* [410 Gone](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#410) - The requested resource is no longer available.<br>
	* [412 Precondition Failure](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#412-precondition-failure) - The operation specified an eTag that is different from the version available at the server, that is, an optimistic concurrency error. Retry the request after reading the latest version of the resource and updating the eTag on the request.<br>
	* [415 Unsupported Media Type](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#415-unsupported-media-type) - The payload format sent by the client is in an unsupported format.<br>
	* [416 Range Not Satisfiable](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#416-range-not-satisfiable)<br>
	* [500 Internal Server Error](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#500-internal-server-error)<br>
	* [503 Service Unavailable](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-error-codes#503-service-unavailable) - The server is currently unable to receive requests. This error may be caused by excessive requests to the service. Media Services throttling mechanism restricts the resource usage for applications that make excessive request to the service. Check the error message and error code string to get more detailed information about the reason you got the 503 error. This error does not always mean throttling.




