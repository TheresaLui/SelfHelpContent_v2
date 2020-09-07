<properties
	pageTitle="Metrics are not available or are incorrect"
	description="Configuration and Management/Metrics are not available or are incorrect"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581617"
	productPesIds="16170"
	cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="bf000ecb-9268-4834-bb7f-6eced0867de3"
	ownershipId="Compute_AppService"
/>
# Metrics are not available or are incorrect
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
			"displayLabel": "Is the metric only missing for a specific time range view (i.e past hour, past 24 hours etc.)? If yes, please specify the time range in the details.",
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
			"controlType": "textbox",
			"displayLabel": "Which metric is not being shown or is incorrect?",
			"watermarkText": "...",
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---