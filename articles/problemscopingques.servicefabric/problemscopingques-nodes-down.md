<properties
	pageTitle="Cluster nodes down or stuck in disabling"
	description="Cluster nodes down or stuck in disabling"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32690985, 32690986"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-nodes-down"
	ownershipId="Compute_ServiceFabric"
/>
# Cluster nodes down or stuck in disabling
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cluster nodes down or stuck in disabling",
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
			"id": "disabling_steps",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "If you were trying to disable the node, please list the steps that were taken to disable the node.",
			"required": false
		}
	],
    "$schema": "SelfHelpContent"
}
---