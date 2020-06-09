<properties
	pageTitle="Scoping questions for Authentication and authorization"
	description="Authentication and authorization"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32606471"
	productPesIds="16170"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="0b0cb739-3aa0-45da-91c5-17e78c0b33b6"
	ownershipId="Compute_AppService"
/>

# Authentication and authorization
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
			"id": "2",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Are you using ADAL?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
        {
			"id": "3",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Is this a problem managing the App in the Portal?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Are you configuring your application for authentication\\\\authorization using the Portal configuration in Azure App Service?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		},
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
