<properties
	pageTitle="Authentication or access control"
	description="Authentication or access control"
	service="microsoft.media"
	resource="mediaservices"
	authors="akucer"
	ms.author="akucer"
	displayOrder="1"
	articleId="mediaservices-authentication-access-control"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32729543"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>
# Authentication or access control
## Accessing the Azure Media Services API

To be authorized to access Media Services resources and the Media Services API, you must first be authenticated. Media Services supports [Azure Active Directory (Azure AD)-based](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) authentication. Two common authentication options are:
 
* **Service principal authentication**: Used to authenticate a service (for example: web apps, function apps, logic apps, API, and microservices). Applications that commonly use this authentication method are apps that run daemon services, middle-tier services, or scheduled jobs. 
* **User authentication**: Used to authenticate a person who is using the app to interact with Media Services resources. The interactive app should first prompt the user for the user's credentials. An example is a management console app used by authorized users to monitor encoding jobs or live streaming.

The Media Services API requires that the user or app making the REST API requests have access to the Media Services account resource and use a **Contributor** or **Owner** role. The API can be accessed with the **Reader** role but only **Get** or **List**  operations will be available. For more information, see [Role-based access control for Media Services accounts](https://docs.microsoft.com/azure/media-services/latest/rbac-overview).

Instead of creating a service principal, consider using managed identities for Azure resources to access the Media Services API through Azure Resource Manager. To learn more about managed identities for Azure resources, see [What is managed identities for Azure resources](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview).

## **Recommended Documents**
**Media Services v3 (latest)**
* [Develop with Media Services v3 APIs](https://docs.microsoft.com/azure/media-services/latest/media-services-apis-overview)

**Media Services v2 (legacy)**
* [Access the Azure Media Services API with Azure AD authentication](https://docs.microsoft.com/azure/media-services/previous/media-services-use-aad-auth-to-access-ams-api)


