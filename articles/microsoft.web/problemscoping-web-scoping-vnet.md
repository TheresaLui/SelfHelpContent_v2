<properties
	pageTitle="Scoping questions for VNET integration with App Service"
	description="VNET integration with App Service"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32542212"
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="28446461-8c33-42b3-984e-0d378ea3bbf1"
	ownershipId="Compute_AppService"
/>

# VNET integration with App Service
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
			"displayLabel": "Is point-to-site enabled on VNET Gateway?",
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
			"displayLabel": "What is the name of VNET",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "What is the Gateway type configured with existing VNET?",
			"watermarkText": "...",
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---