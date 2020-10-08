<properties
	pageTitle="Application Errors and Exceptions"
	description="Application Errors and Exceptions"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32608950"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-errors-and-exceptions-sf"
	ownershipId="Compute_ServiceFabric"
/>
# Application Errors and Exceptions
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Application Errors and Exceptions",
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
            "watermarkText": "Provide the name of the application.",
            "required": false
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message",
            "watermarkText": "What is the exact error or exception message?",
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---