<properties
	pageTitle="I am getting 401 errors for my API requests"
	description="I am getting 401 errors for my API requests"
	service="microsoft.maps"
	resource="accounts"
	authors="michael-falk"
    resourceTags=""
    selfHelpType="resource"
	supportTopicIds=""
	productPesIds=""
	displayOrder="1"
	cloudEnvironments="public, fairfax, usnat, ussec"
 	articleId="409089c2-08ba-4e74-a96f-1fca90116de4"
	ownershipId="AzureIot_AzureMaps"
/>

# I am getting 401 errors for my API requests 

## **Recommended Steps**

1. The API  keys you are using may not have been correctly sent in the header or query string. For example, put key into "Ocp-Apim-Subscription-Key" header or in "Subscription-Key={key}" in query string when sending a HTTP POST request.
2. Check Azure subscription status to ensure its active. Click on "Subscriptions" to see the Subscription blade and check the status.
3. Review the specific API documentation to find details on specific error codes.

## **Recommended Documents**

- [Azure Maps Documentation](https://go.microsoft.com/fwlink/?linkid=862272) 
