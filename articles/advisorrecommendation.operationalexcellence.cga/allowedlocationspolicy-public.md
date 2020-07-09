<properties
    pageTitle="Enforce 'Allowed locations' using Azure Policy."
    description="Azure Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources. This policy enables you to restrict the locations your organization can specify when deploying resources. Use to enforce your geo-compliance requirements."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="6d395b56-af36-4f01-a814-f8ba08e49c26_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"	ownershipId="CGA_DataPlatform"
/>
# Enforce 'Allowed locations' using Azure Policy
---
{
	"recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
	"recommendationOfferingName": "Azure Advisor",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "6d395b56-af36-4f01-a814-f8ba08e49c24",
	"dataSourceMetadata": {
		"schemaVersion": 2.0,
		"dataSource": "SAS"
	},
	"recommendationCategory": "OperationalExcellence",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
	"recommendationFriendlyName": "AllowedLocationsPolicy",
	"recommendationMetadataState": "Active",
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
	"ingestionClientIdentities": [
		"397d7011-8a0c-4165-a3f5-8d4e5f2e676d"
	],
	"recommendationTimeToLive": 86400,
	"version": 2.0,
	"learnMoreLink": "https://docs.microsoft.com/azure/governance/policy/overview",
	"description": "Enforce 'Allowed locations' using Azure Policy",
	"longDescription": "Azure Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources. This policy enables you to restrict the locations your organization can specify when deploying resources. Use to enforce your geo-compliance requirements.",
	"potentialBenefits": "This specific policy restricts the available locations where your organization can deploy new resources.",
	"actions": [
		{
			"actionId": "f8db3c62-8ed7-48ea-b313-83c7224a5c48",
			"description": "Assign the 'Allowed locations' policy",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_Policy",
			"bladeName": "PolicyDetailBlade",
			"metadata": {
				"definitionId": "/providers/Microsoft.Authorization/policyDefinitions/e56962a6-4747-49cd-b67b-bf8b01975c4c"
			}
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "ea5d42fe-bc1f-491c-a7e2-b1b172188bf7",
			"actionType": "Blade",
			"extensionName": "HubsExtension",
			"bladeName": "ResourceMenuBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Assign the 'Allowed locations' policy",
	"additionalColumns": [],
	"tip": "Azure Policy allows IT admins to define, assign, and, manage standards for resources in their environment."
}
---
