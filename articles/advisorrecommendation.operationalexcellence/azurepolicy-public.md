<properties
    pageTitle="Create Azure Policy recommendation"
    description="Create Azure Policy recommendation"
    authors="timwong"
    ms.author="timwong"
    articleId="84bd72c6-7596-4806-84c4-bc39fe3967f8"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Create Azure policy
---
{
	"recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
	"recommendationOfferingName": "Azure Advisor",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "84bd72c6-7596-4806-84c4-bc39fe3967f8",
	"dataSourceMetadata": {
		"schemaVersion": 2.0,
		"dataSource": "SAS"
	},
	"recommendationCategory": "HighAvailability",
	"recommendationImpact": "Low",
	"recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
	"recommendationFriendlyName": "AzurePolicy",
	"recommendationMetadataState": "Disabled",
	"portalFeatures": [],
	"owner": {
		"email": "cga-sup@microsoft.com",
		"icm": {
			"routingId": "MDM://CGAAdvisorRecommendations",
			"service": "CGA Data Science",
			"team": "CGAAdvisorRecommendations"
		},
		"serviceTreeId": "0dbc6a29-122a-4ab5-8070-5868a2bcd57b"
	},
	"ingestionClientIdentities": [ "8d7ef949-acae-4519-88ea-426d131ba6ab" ],
	"recommendationTimeToLive": 86400,
	"version": 2.0,
	"learnMoreLink": "https://docs.microsoft.com/azure/governance/policy/overview",
	"description": "Configure Azure Policy over your Azure resources",
	"longDescription": "Configure Azure Policy over your Azure resources to stay compliant with your coporate standards and service level agreements.",
	"potentialBenefits": "Stay compliant with your coporate standards and service level agreements",
	"actions": [
		{
			"actionId": "e10b9c32-5af9-40cd-9b04-caca22bad08d",
			"description": "Create Azure Policy",
			"actionType": "Document",
			"documentLink": "https://docs.microsoft.com/azure/governance/policy/overview"
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "85a84769-6030-49b9-9fdc-5c10fe1087f9",
			"actionType": "Blade",
			"extensionName": "HubsExtension",
			"bladeName": "ResourceMenuBlade",
			"metadata": { "id": "{resourceId}" }
		}
	},
	"displayLabel": "Configure Azure Policy",
	"additionalColumns": [],
	"tip": "You can configure Azure Policy to enforce rules over your resources to stay complaint.",
	"testData": "36d32aaa-efe0-454b-9326-e5547b655dba,/subscriptions/36d32aaa-efe0-454b-9326-e5547b655dba"
}
---
