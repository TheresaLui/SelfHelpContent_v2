<properties
	pageTitle="AAD"
	description="AAD Configuration"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32608940"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-aad"
	ownershipId="Compute_ServiceFabric"
/>
# AAD Configuration
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "AAD Configuration",
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
            "id": "failure_reason",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Authentication Failure",
            "watermarkText": "Provide any error codes that appear when trying to access your cluster resource through AAD.",
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---