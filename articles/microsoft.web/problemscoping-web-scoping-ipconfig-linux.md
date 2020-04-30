<properties
	pageTitle="Scoping questions for IP configuration"
	description="IP configuration"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32542210"
	productPesIds="16170"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="1b5ede53-4f95-933f-92355b9f7e7f"
	ownershipId="Compute_AppService"
/>

# IP configuration
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
			"controlType": "textbox",
			"displayLabel": "Are you looking to set up IP restrictions or are the current settings not working?",
			"watermarkText": "...",
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---