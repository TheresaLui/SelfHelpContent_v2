<properties
	pageTitle="Scoping questions for WordPress"
	description="WordPress"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32444080"
	productPesIds="16333"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="be52-4ad7-8b99-8236841af287"
	ownershipId="Compute_AppService"
/>

# WordPress
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
			"displayLabel": "Have you enabled WordPress debug.log and PHP error log?",
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
		}
    ],
    "$schema": "SelfHelpContent"
}
---