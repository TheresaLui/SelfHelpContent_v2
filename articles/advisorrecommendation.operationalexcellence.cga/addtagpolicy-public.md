<properties
    pageTitle="Enforce 'Add or replace a tag on resources' using Azure Policy"
    description="Azure Policy will help define, assign and manage standards for resources in your environment. This specific policy allows for resources to be tagged or for tagged to be replaced."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="bbd39b95-99d9-4b7e-b66b-8813081307c8_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"	ownershipId="CGA_DataPlatform"
/>
# Enforce 'Add or replace a tag on resources' using Azure Policy
---
{
	"recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
	"recommendationOfferingName": "Azure Advisor",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "bbd39b95-99d9-4b7e-b66b-8813081307c1",
	"dataSourceMetadata": {
		"schemaVersion": 2.0,
		"dataSource": "SAS"
	},
	"recommendationCategory": "OperationalExcellence",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
	"recommendationFriendlyName": "AddTagPolicy",
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
	"description": "Enforce 'Add or replace a tag on resources' using Azure Policy",
	"longDescription": "Azure Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources. This policy adds or replaces the specified tag and value when any resource is created or updated. Existing resources can be remediated by triggering a remediation task. Does not modify tags on resource groups.",
	"potentialBenefits": "This specific policy allows for resources to be tagged or for tags to be replaced.",
	"actions": [
		{
			"actionId": "f59d0214-294c-4e6e-9e1b-e7b7ff871b1f",
			"description": "Assign the 'Add or replace a tag on resources' policy",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_Policy",
			"bladeName": "PolicyDetailBlade",
			"metadata": {
				"definitionId": "/providers/Microsoft.Authorization/policyDefinitions/5ffd78d9-436d-4b41-a421-5baa819e3008"
			}
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "e10cefce-736b-42ac-aa85-70c87ca10dc6",
			"actionType": "Blade",
			"extensionName": "HubsExtension",
			"bladeName": "ResourceMenuBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Assign the 'Add or replace a tag on resources' policy",
	"additionalColumns": [],
	"tip": "Azure Policy allows IT admins to define, assign, and, manage standards for resources in their environment."
}
---
