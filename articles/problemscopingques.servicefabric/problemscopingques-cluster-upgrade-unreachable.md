<properties
	pageTitle="Upgrade Service Unreachable"
	description="Upgrade Service Unreachable"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32690991"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-cluster-upgrade-unreachable"
	ownershipId="Compute_ServiceFabric"
/>
# Upgrade Service Unreachable
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Upgrade Service Unreachable",
    "fileAttachmentHint": "Please attach the ARM template used to deploy the cluster as well as any relevant logs/screenshots.",
    "formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
		{
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		},
        {
			"id": "networking_rules",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Do you have any networking rules that block outbound traffic from the cluster?",
			"required": false
		}
	],
    "$schema": "SelfHelpContent"
}
---