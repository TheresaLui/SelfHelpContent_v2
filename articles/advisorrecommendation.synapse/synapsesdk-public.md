<properties
    pageTitle="Upgrade SDK version recommendation"
    description="Return list of resources that do not currently use the recommended SDK version"
    ms.author="srthatip"
    articleId="7c83695a-3fa9-4668-9080-85151f5ab7be_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,usnat,ussec"
    ownershipId="AzureData_SynapseAnalytics"
/>
# SynapseManagementClient SDK Version Recommendation
---
{
	"recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
	"recommendationOfferingName": "Azure Synapse Analytics",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "7c83695a-3fa9-4668-9080-85151f5ab7be",
	"dataSourceMetadata": {
		"streamNamespace": "cluster('https://analytics365prod.kusto.windows.net').database('Analytics365PROD').synapse_advisor_SynapseManagementClientSdk",
		"dataSource": "Kusto",
		"refreshInterval": "0.12:00:00"
	},
	"recommendationCategory": "Performance",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.Synapse/workspaces",
	"recommendationFriendlyName": "UpgradeSynapseManagementClientSDK",
	"recommendationMetadataState": "Active",
	"owner": {
		"email": "a365rp@microsoft.com",
		"icm": {
		  "routingId": "mdm://adspartner/AzureSynapsePlateform/SynapseProvider",
		  "service": "Azure Synapse Platform Service",
		  "team": "Synapse Resource Provider"
		},
		"serviceTreeId": "c0ee70d5-102d-438c-8858-795b92dc0f99"
	},
	"version": 6.0,
	"learnMoreLink": "https://aka.ms/UpgradeSynapseManagementClientSDK",
	"description": "Update SynapseManagementClient SDK Version",
	"longDescription": "New SynapseManagementClient is using .NET SDK 4.0 or above.",
	"potentialBenefits": "Latest SynapseManagementClient Libraries contain fixes for known issues and additional improvements.",
	"supportedSDKLanguages": [".Net"],
	"actions": [
		{
			"actionId": "7c83695a-3fa9-4668-9080-85151f5ab8be",
			"description": "Learn how to update your SynapseManagementClient Libraries",
			"actionType": "Document",
			"documentLink": "{recommendedActionLearnMore}"
		},
		{
			"actionId": "7c83695a-3fa9-4668-9080-85151f5ab9be",
			"description": "View {version} release notes",
			"actionType": "Document",
			"documentLink": "{releaseNotes}"
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "7c83695a-3fa9-4668-9080-85151f5ab6be",
			"actionType": "Blade",
			"extensionName": "HubsExtension",
			"bladeName": "ResourceMenuBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Update SynapseManagementClient",
	"additionalColumns": [{
			"name": "language",
			"title": "SDK Language"
		},
		{
			"name": "version",
			"title": "Minimum Recommended Version"
		}
	],
	"tip": ""
}
---
