<properties
	pageTitle="Scoping questions for PHP"
	description="PHP"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32444083"
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="793d003c-aff7-4810-9edf-8bbeccf38e7c"
	ownershipId="Compute_AppService"
/>

# PHP
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
			"displayLabel": "Have you enabled PHP error log?",
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