<properties
	pageTitle="Application Deployment"
	description="Application Deployment"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32608937"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-application-deployment-sf"
	ownershipId="Compute_ServiceFabric"
/>
# Application Deployment
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Application Deployment",
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
            "id": "register_or_copy_error",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Did any errors occur during the copy or registering operations while deploying the application?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                "value": "Yes",
                "text": "Yes"
            },
            {
                "value": "No",
                "text": "No"
            }],
            "required": false
        },
        {
            "id": "error_timestamp",
            "order": 5,
            "visibility": "register_or_copy_error == Yes",
            "controlType": "datetimepicker",
            "displayLabel": "What time was the deployment?",
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---