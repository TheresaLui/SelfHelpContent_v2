<properties
	pageTitle="Application"
	description="Application"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32690999, 32690980, 32691001, 32690987, 32690983, 32690981, 32690992"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-application-sf"
	ownershipId="Compute_ServiceFabric"
/>
# Application
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Application",
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
        }
	],
    "$schema": "SelfHelpContent"
}
---