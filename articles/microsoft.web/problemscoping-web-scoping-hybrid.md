<properties
	pageTitle="Scoping questions for Configuring hybrid connections with App Service"
	description="Configuring hybrid connections with App Service"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581613"
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="e1e848fd-cac2-4473-81a4-b523796daf93"
	ownershipId="Compute_AppService"
/>

# Configuring hybrid connections with App Service
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
			"displayLabel": "What is the status of the HC?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Not connected",
					"text": "Not connected"
				}, {
					"value": "Connected",
					"text": "Connected"
				}, {
					"value": "Status unknown",
					"text": "Status unknown"
				}
			],
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the Hybrid Connection URL? (You can find this in the Hybrid Connection Manager details for the HC or in the connection string shown in the portal)",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "What is the HC endpoint? (The endpoint that is visible in the Azure portal)",
			"watermarkText": "...",
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---
