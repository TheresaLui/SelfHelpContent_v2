<properties
	pageTitle="Scale Stream Analytics cluster"
	description="Scale Stream Analytics cluster"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="clusters"
	authors="sidramadoss"
	articleId="streamanalytics-scalecluster"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32756393"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Scale Stream Analytics cluster

ASA clusters can meet you changing streaming capacity requirements by allowing you to scale up/down your cluster size. Changing the scale of cluster is a long running operation and is not intended to be autoscalable. It is recommended to provision the right number of SUs ahead of time to meet your needs.

The minimum size of a Stream Analytics cluster is 36 SUs and the maximum you can scale to now is 216 SUs. If you require more than 216 SUs in a cluster, please file a support ticket and we can provision one for you.

If you are looking for cluster with granular SU options between 36 and 216 that aren't available in the scale settings, please reach out to us at askasa@microsoft.com

To learn more about scaling clusters, see the recommended documents.

## **Recommended Documents**

* [How to scale Stream Analytics cluster](https://docs.microsoft.com/azure/stream-analytics/scale-cluster)
