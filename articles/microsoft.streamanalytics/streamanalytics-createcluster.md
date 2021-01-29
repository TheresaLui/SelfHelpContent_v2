<properties
	pageTitle="Create Stream Analytics cluster"
	description="Create Stream Analytics cluster"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="clusters"
	authors="sidramadoss"
	articleId="streamanalytics-createcluster"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32756387"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Create Stream Analytics cluster

Stream Analytics clusters are powered by the same engine that powers Stream Analytics jobs running in a multi-tenant environment. Creating clusters is expected to be a long running operation that could take 60 minutes or more depending on the capacity chosen.

### Frequently asked questions
1. Why has my cluster creation not completed for a long time?
The reason for the long time to create is because, we create a dedicated VNet behind the scenes inside which all the necessary resources are provisioned and setup ready for you to run your Stream Analytics jobs.

2. When will I get charged for my clusters?
You will be [charge](https://azure.microsoft.com/pricing/details/stream-analytics/) for the cluster immediately after the cluster is created and usable. You will be charged even if there no streaming jobs running on it. 

3. When should I create a cluster?
If you want to connect ASA jobs to other resources using private endpoints, then creating a cluster is one way to get started using Stream Analytics. Alternatively, you can [download ASA tools for Visual Studio](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-tools-for-visual-studio-install) to develop and [test jobs locally](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-live-data-local-testing) on your device using live data from the cloud. And once you are ready to run jobs in the cloud with private endpoints, you can then create cluster.

To learn more about activity logs, see the recommended documents.

## **Recommended Documents**

* [How to create Stream Analytics cluster](https://docs.microsoft.com/azure/stream-analytics/create-cluster)
