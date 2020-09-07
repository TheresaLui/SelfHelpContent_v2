<properties
	pageTitle="Scoping questions for Web app restarted"
	description="Web app restarted"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32570954"
	productPesIds="16170"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="84fdb6ef-457d-9c12-4b83f9f95802"
	ownershipId="Compute_AppService"
/>

# Web app restarted
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
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Have you seen any application errors during the restart timeframe? If so, what was the error?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "What is the frequency of the restarts?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "6",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Is the issue still occurring? If not, how was the issue resolved?",
			"watermarkText": "...",
			"required": false
		}],
    "$schema": "SelfHelpContent"
}
---
