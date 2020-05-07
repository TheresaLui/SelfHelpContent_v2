<properties
	pageTitle="Scoping questions for Configuring custom domain names"
	description="Configuring custom domain names"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32440122"
	productPesIds="16170"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="9314bc56-da73-49ab-951c-93cba03e0ab6"
	ownershipId="Compute_AppService"
/>

# Configuring custom domain names

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
			"displayLabel": "Is this an App Service Domain or an externally hosted domain?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "App Service Domain",
					"text": "App Service Domain"
				}, {
					"value": "Externally hosted domain",
					"text": "Externally hosted domain"
				}
			],
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the custom domain?",
			"watermarkText": "...",
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---