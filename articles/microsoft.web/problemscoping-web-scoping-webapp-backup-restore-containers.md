<properties
	pageTitle="Scoping questions for Backup and Restore"
	description="Backup and Restore"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32542208"
	productPesIds="16333"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="69353d19-4a89-8e61-a74482e15"
	ownershipId="Compute_AppService"
/>

# Backup and Restore
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
			"displayLabel": "Is it a Scheduled Backup or Manual Backup?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Scheduled",
					"text": "Scheduled"
				}, {
					"value": "Manual",
					"text": "Manual"
				}
			],
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---
