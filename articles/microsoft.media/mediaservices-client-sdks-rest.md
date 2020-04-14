<properties
	pageTitle="Azure Media Services REST API"
	description="Azure Media Services REST API"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-sdks-rest"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632119"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>
# Azure Media Services REST API

## **Recommended Steps**

**Using the v3 REST API**

1. Get information needed to [access the v3 APIs](https://docs.microsoft.com/azure/media-services/latest/access-api-cli-how-to)
2. Download and install the [Postman REST client application](https://www.getpostman.com/)
   
   - We are using Postman, but any REST client tool would be suitable. Other alternatives are Visual Studio Code with the REST plugin or Telerik Fiddler.
  
3. Review the article on how to [configure Postman](https://docs.microsoft.com/azure/media-services/latest/media-rest-apis-with-postman)
4. Update access variables in Postman with values you got from the Access the Media Services API in step #1.
5. Use "Step 1" in the Postman collection to get the AAD authentication token first before attempting to use any other APIs. This will create a JWT token for use in authentication of each API call.

   **NOTE**: The JWT token returned is valid for 1 hour. Refresh the token upon expiration. 
   
6. Use the API examples in the Postman collection to learn how the Media Services v3 API works


## **Recommended Documents**

**Version 3 REST API (latest)**

- [Version 3 REST API Reference documentation](https://docs.microsoft.com/rest/api/media/accountfilters)<br>
- [Get started with the REST API using the Postman collection](https://docs.microsoft.com/azure/media-services/latest/media-rest-apis-with-postman)<br>
- [Start developing with client SDKs that wrap the REST API](https://docs.microsoft.com/azure/media-services/latest/developers-guide)
  
**Version 2 REST API (legacy)**

  - [Overview of the v2 REST API](https://docs.microsoft.com/azure/media-services/previous/media-services-rest-how-to-use)<br>
  - [Version 2 REST API Reference](https://docs.microsoft.com/rest/api/media/operations/azure-media-services-rest-api-reference)<br>
  - [How to access the v2 REST API with AAD](https://docs.microsoft.com/azure/media-services/previous/media-services-rest-connect-with-aad)<br>
  - [Version 2 Postman Collection](https://docs.microsoft.com/azure/media-services/previous/media-rest-apis-with-postman)<br>

