<properties
    pageTitle="Enforce 'Inherit a tag from the resource group' using Azure Policy"
    description="Azure Policy will help define, assign and manage standards for resources in your environment. This specific policy allows for resources to inherit tags from the parent resource group."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="b2c74ac7-061e-4164-b272-ecb0940f5966_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"	ownershipId="CGA_DataPlatform"
/>
# Enforce 'Inherit a tag from the resource group' using Azure Policy
---
{
	"recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
	"recommendationOfferingName": "Azure Advisor",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "b2c74ac7-061e-4164-b272-ecb0940f5965",
	"dataSourceMetadata": {
		"schemaVersion": 2.0,
		"dataSource": "SAS"
	},
	"recommendationCategory": "OperationalExcellence",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
	"recommendationFriendlyName": "InheritTagPolicy",
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
	"description": "Enforce 'Inherit a tag from the resource group' using Azure Policy",
	"longDescription": "Azure Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources. This policy adds or replaces the specified tag and value from the parent resource group when any resource is created or updated. Existing resources can be remediated by triggering a remediation task.",
	"potentialBenefits": "This specific policy allows for resources to inherit tags from the parent resource group.",
	"actions": [
		{
			"actionId": "8e0a665f-5f93-4417-abb3-0a9ed788e999",
			"description": "Assign the 'Inherit a tag from the resource group' policy",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_Policy",
			"bladeName": "PolicyDetailBlade",
			"metadata": {
				"definitionId": "/providers/Microsoft.Authorization/policyDefinitions/cd3aa116-8754-49c9-a813-ad46512ece54"
			}
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "eca2d0cf-39a0-4465-b005-a2327b8e4618",
			"actionType": "Blade",
			"extensionName": "HubsExtension",
			"bladeName": "ResourceMenuBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Assign the 'Inherit a tag from the resource group' policy",
	"additionalColumns": [],
	"tip": "Azure Policy allows IT admins to define, assign, and, manage standards for resources in their environment."
}
---
