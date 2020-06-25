<properties
    pageTitle="Enforce 'Allowed virtual machine SKUs' using Azure Policy."
    description="Azure Policy will help define, assign and manage standards for resources in your environment. This specific policy restricts the virtual machine SKUs that your organizations can deploy."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="56089005-f16c-4b41-ba0d-2eb3549292d2_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"	ownershipId="CGA_DataPlatform"
/>
# Enforce 'Allowed virtual machine SKUs' using Azure Policy
---
{
	"recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
	"recommendationOfferingName": "Azure Advisor",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "56089005-f16c-4b41-ba0d-2eb3549292d5",
	"dataSourceMetadata": {
		"schemaVersion": 2.0,
		"dataSource": "SAS"
	},
	"recommendationCategory": "OperationalExcellence",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
	"recommendationFriendlyName": "AllowedVirtualMachineSkuPolicy",
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
	"description": "Enforce 'Allowed virtual machine SKUs' using Azure Policy",
	"longDescription": "Azure Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources. This policy enables you to specify a set of virtual machine SKUs that your organization can deploy.",
	"potentialBenefits": "This specific policy restricts the virtual machine SKUs that your organization can deploy.",
	"actions": [
		{
			"actionId": "fed5602b-707c-4944-aac9-b779e0154bfd",
			"description": "Assign the 'Allowed virtual machine SKUs' policy",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_Policy",
			"bladeName": "PolicyDetailBlade",
			"metadata": {
				"definitionId": "/providers/Microsoft.Authorization/policyDefinitions/cccc23c7-8427-4f53-ad12-b6a63eb452b3"
			}
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "d9838bfb-8369-4341-ab34-318ee6a16e22",
			"actionType": "Blade",
			"extensionName": "HubsExtension",
			"bladeName": "ResourceMenuBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Assign the 'Allowed virtual machine SKUs' policy",
	"additionalColumns": [],
	"tip": "Azure Policy allows IT admins to define, assign, and, manage standards for resources in their environment."
}
---
