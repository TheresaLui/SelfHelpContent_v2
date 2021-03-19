<properties
	pageTitle="Create private endpoints in Stream Analytics cluster"
	description="Create private endpoints in Stream Analytics cluster"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="clusters"
	authors="sidramadoss"
	articleId="streamanalytics-createpe"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32756388"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Create private endpoints in Stream Analytics cluster

You can connect your Azure Stream Analytics jobs running on a cluster to input and output resources that are behind a firewall or an Azure Virtual Network (VNet). First, you create a private endpoint for a resource, such as Azure Event Hub or Azure SQL Database, in your Stream Analytics cluster. Then, approve the private endpoint connection from your input or output.

Once you approve the connection, any job running in your Stream Analytics cluster has access the resource through the private endpoint. This article shows you how to create and delete private endpoints in a Stream Analytics cluster.

### Frequently asked questions
1. Why does the private endpoint I created doesn't show up in the input/output resource for me to approve?
When you create your first private endpoint in your cluster, it might take few minutes for the private endpoint to get created and the request to show up in the resource (e.g., SQL DB, Event Hubs etc). If this takes more than 5 minutes, please create a support ticket.

2. Will I be charged for private endpoints?
You are not charged extra for private endpoints but will be charged in line with Azure Private Link pricing model.

3. Even after approving the request from the input/output resource side, I still see "pending customer approval". Why?
It might take up to a minute or two for the state to reflect approval and for the setup to complete. If it shows "pending customer approval" for longer than 5 minutes of you manually approving it from the input/output resource side, please create a support ticket. 

To learn more about activity logs, see the recommended documents.

## **Recommended Documents**

* [How to create private endpoints](https://docs.microsoft.com/azure/stream-analytics/private-endpoints)
