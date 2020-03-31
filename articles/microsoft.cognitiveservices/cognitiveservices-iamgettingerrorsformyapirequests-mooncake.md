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
    cloudEnvironments="MoonCake"
	articleId="4074b1f1-f5cb-4472-8f70-0f4f7735c7ce"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# I am getting 401 errors for my API requests

## **Recommended steps**

To troubleshoot common issues related to Cognitive Services API requests, please try the following options:

1. The API  keys you are using may not have been correctly sent in the header or query string. For example, put key into "Ocp-Apim-Subscription-Key" header or in "Subscription-Key={key}" in query string when sending a HTTP POST request.
2. Check Azure subscription status to ensure its active by checking the Subscriptions status in [Azure Portal](https://portal.azure.cn).
3. Review the specific API documentation to find details on specific error codes.

## **Recommended documents**

* [Cognitive Services documentation](https://docs.azure.cn/cognitive-services/)
