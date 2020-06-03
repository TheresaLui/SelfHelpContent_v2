<properties
    pageTitle="Enforce 'Audit VMs that do not use managed disks' using Azure Policy."
    description="Azure Policy will help define, assign and manage standards for resources in your environment. This specific policy audits VMs that do not use managed disks."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="142bcb82-aa8d-44e8-98d4-2b39125f2322_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"	ownershipId="CGA_DataPlatform"
/>
# Enforce 'Audit VMs that do not use managed disk' using Azure Policy
---
{
	"recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
	"recommendationOfferingName": "Azure Advisor",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "142bcb82-aa8d-44e8-98d4-2b39125f2324",
	"dataSourceMetadata": {
		"schemaVersion": 2.0,
		"dataSource": "SAS"
	},
	"recommendationCategory": "OperationalExcellence",
	"recommendationImpact": "High",
	"recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
	"recommendationFriendlyName": "AuditForManagedDisksPolicy",
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
	"description": "Enforce 'Audit VMs that do not use managed disks' using Azure Policy",
	"longDescription": "Azure Policy is a service in Azure that you use to create, assign, and manage policies. These policies enforce different rules and effects over your resources. This policy audits VMs that do not use managed disks.",
	"potentialBenefits": "This specific policy audits VMs that do not use managed disks.",
	"actions": [
		{
			"actionId": "78af20c0-31ea-450c-9ad2-bda2294f9ca7",
			"description": "Assign the 'Audit VMs that do not use managed disks' policy",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_Policy",
			"bladeName": "PolicyDetailBlade",
			"metadata": {
				"definitionId": "/providers/Microsoft.Authorization/policyDefinitions/06a78e20-9358-41c9-923c-fb736d382a4d"
			}
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "2d00b97a-7d21-4aaf-be07-1a441c2c90d2",
			"actionType": "Blade",
			"extensionName": "HubsExtension",
			"bladeName": "ResourceMenuBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Enforce 'Audit VMs that do not use managed disks' using Azure Policy",
	"additionalColumns": [],
	"tip": "Azure Policy allows IT admins to define, assign, and, manage standards for resources in their environment."
}
---
