<properties
	pageTitle="Connect via private endpoints in Stream Analytics cluster"
	description="Connect via private endpoints in Stream Analytics cluster"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="clusters"
	authors="sidramadoss"
	articleId="streamanalytics-connectpe"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32756391"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Connect via private endpoints in Stream Analytics cluster

Private endpoints created in a cluster can be used any job running on your cluster. Setting up private endpoints is a 2 step process.
1. Create private endpoint in your Stream Analytics cluster that maps to your input/output resource (e.g., Azure Event hubs, SQL DB etc)
2. Goto the input/output resource (e.g., Azure Event hubs, SQL DB etc) and then approve the private endpoint connection. Return to your cluster and see that the PE has been setup successfully.

To learn more about private endpoints, see the recommended documents.

## **Recommended Documents**

* [How to create and delete private endpoints](https://docs.microsoft.com/azure/stream-analytics/private-endpoints)
