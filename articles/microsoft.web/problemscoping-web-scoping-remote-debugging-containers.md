<properties
	pageTitle="Scoping questions for Remote debugging"
	description="Remote debugging"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581620"
	productPesIds="16333"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="2039-452c-a39b-028cde102221"
	ownershipId="Compute_AppService"
/>

# Remote debugging
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
			"displayLabel": "Have you updated Visual Studio to the latest updates?",
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
			"displayLabel": "Have you updated the Azure SDK to the latest updates?",
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
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "What is the version and release of Visual Studio you are using?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "6",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Are you using Cloud Explorer to start debugging or manually attaching the debugger?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Cloud Explorer",
					"text": "Cloud Explorer"
				}, {
					"value": "Manual",
					"text": "Manual"
				}
			],
			"required": false
		},
        {
			"id": "7",
			"order": 7,
			"controlType": "textbox",
			"displayLabel": "What is the exact error message?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "8",
			"order": 8,
			"controlType": "dropdown",
			"displayLabel": "Are you behind a firewall?",
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