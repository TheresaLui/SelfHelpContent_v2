<properties
	pageTitle="Scoping questions for Web app slow"
	description="Web app slow"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32457411"
	productPesIds="16170"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="a9219edd-4dc7-9b67-099847303e2a"
	ownershipId="Compute_AppService"
/>

# Web app slow
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
			"displayLabel": "Is the issue intermittent or consistent? If intermittent, please explain in the additional details the observed pattern",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "intermittent",
					"text": "intermittent"
				}, {
					"value": "consistent",
					"text": "consistent"
				}
			],
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Which URL(s) are experiencing the slowdown?",
			"watermarkText": "...",
			"required": false
		},
         {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Is the issue still occurring? If not, how was the issue resolved??",
			"watermarkText": "...",
			"required": false
		}],
    "$schema": "SelfHelpContent"
}
---

