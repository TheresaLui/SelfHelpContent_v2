<properties
	pageTitle="I am getting 401 errors for my API requests"
	description="I am getting 401 errors for my API requests"
	service="microsoft.cognitiveservices"
	resource="accounts"
	authors="kasparks"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="df609b4e-bb37-4e41-9846-6ff5eec87a2e"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# I am getting 401 errors for my API requests

## **Recommended steps**
To resolve the most common issues, try one or more of the following steps.

1. The API  keys you are using may not have been correctly sent in the header or query string. For example, put key into 
"Ocp-Apim-Subscription-Key" header or in "Subscription-Key={key}" in query string when sending a HTTP POST request.
2. Check Azure subscription status to ensure its active.<br>
Click on "Subscriptions" to see the Subscription blade and check the status.
3. Review the specific API documentation to find details on specific error codes.

## **Recommended documents**
[Cognitive Services documentation](https://www.microsoft.com/cognitive-services/en-us/documentation)
