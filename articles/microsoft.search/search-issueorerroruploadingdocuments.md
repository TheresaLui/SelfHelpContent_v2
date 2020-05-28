<properties
	pageTitle="Search Index/Issue indexing documents using the REST API"
	description="Search Index/Issue indexing documents using the REST API"
	service="microsoft.search"
	resource="searchservices"
	authors="bernitorres, mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	supportTopicIds="32681367"
	displayOrder="3"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="07fdc3ea-3445-495a-8ae6-f33ff93a3f37"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue indexing documents using the REST API

## **Recommended Steps**

If you are having trouble indexing documents using the Azure Search REST API, pay close attention to the [HTTP status codes](https://docs.microsoft.com/rest/api/searchservice/http-status-codes) returned in the response. The various per-document codes returned are listed below. Some indicate problems with the request itself, while others indicate temporary error conditions that may go away when you retry after a delay.

* 200: Document was successfully modified or deleted. Delete operations are [idempotent](https://en.wikipedia.org/wiki/Idempotence). Even if a document key does not exist in the index, attempting a delete operation with that key will result in a 200 status code.
* 201: Document was successfully created
* 400: There was an error in the request preventing a document from being indexed. The error message will indicate what is wrong with the request. Correct the error and try again.
* 404: The document could not be updated because the given key doesn't exist in the index. This error does not occur for the upload or merge actions since they will create new documents if the key doesn't exist.
* 409: A version conflict was detected when attempting to index a document. This can happen when you're trying to index the same document more than once concurrently.
* 422: The index is temporarily unavailable because it was updated with the 'allowIndexDowntime' flag set to 'true'. Wait until the operation is complete and try again.
* 429: You have exceeded the storage quota allocated for your service. You can receive this error when uploading new documents or changing existing ones. You must either delete documents, add partitions, or move to a higher service tier for additional quota.
* 503: Your search service is temporarily unavailable, most likely due to heavy load. Your code should wait before retrying in this case or you risk prolonging the service unavailability.

## **Recommended Documents**

* [How to import data into Azure Search - push and pull methods](https://docs.microsoft.com/azure/search/search-what-is-data-import) <br>
* [How to upload documents using the REST API](https://docs.microsoft.com/rest/api/searchservice/AddUpdate-or-Delete-Documents) <br>
* [How to upload documents using indexers with the REST API](https://docs.microsoft.com/rest/api/searchservice/Indexer-operations) <br>
* [How to upload documents using indexers from the portal](https://docs.microsoft.com/azure/search/search-import-data-portal) <br>
* [How to upload documents using the .NET SDK](https://docs.microsoft.com/azure/search/search-howto-dotnet-sdk#core-scenarios) <br>
* [How to index complex data types](https://docs.microsoft.com/azure/search/search-howto-complex-data-types)
