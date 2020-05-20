<properties
	pageTitle="Performance"
	description="Performance"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32608938, 32608958, 32608934"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-performance-sf"
	ownershipId="Compute_ServiceFabric"
/>
# Performance
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Application Performance",
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
            "id": "application_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Application Name",
            "watermarkText": "Provide the name of the application that this is related to.",
            "required": false
        },
        {
            "id": "partition_id",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "PartitionId(s)",
            "watermarkText": "What PartitionId(s) are you seeing the warning on?",
            "required": false
        },
        {
            "id": "node_names",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Nodes",
            "watermarkText": "Which nodes are the warnings coming from?",
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---