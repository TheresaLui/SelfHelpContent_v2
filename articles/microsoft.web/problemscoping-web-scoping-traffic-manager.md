<properties
	pageTitle="Scoping questions for Configuring Traffic Manager with App Service"
	description="Configuring Traffic Manager with App Service"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581614"
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="e62fbea6-244e-4ac6-823e-1f6bce95f331"
	ownershipId="Compute_AppService"
/>

# Configuring Traffic Manager with App Service
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {
            "id": "3",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Are you configuring the App Service(s) as Azure Endpoints or External Endpoints?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Azure Endpoints",
					"text": "Azure Endpoints"
				}, {
					"value": "External Endpoints",
					"text": "External Endpoints"
				}
			],
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the name of Traffic Manager Profile?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "What is the name of the App Service(s) you are configuring Traffic Manager with?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "6",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "What is the custom domain you are configuring with the Traffic Manager URL?",
			"watermarkText": "...",
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---