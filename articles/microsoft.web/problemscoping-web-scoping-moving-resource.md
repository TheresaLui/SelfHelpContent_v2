<properties
	pageTitle="Scoping questions for Moving resources"
	description="Moving resources"
	service="microsoft.web"
	authors="shrahman, khaled-zayed"
    ms.author="shrahman, khzayed"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581619"
	productPesIds="14748"
	cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="73799750-2889-45e0-b6ea-ddb118e38d07"
	ownershipId="Compute_AppService"
/>

# Moving resources
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
			"displayLabel": "Are you moving App Service resources within the same subscription or are you trying to move resources across different subscriptions?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Same Subscription",
					"text": "Same Subscription"
				}, {
					"value": "Different Subscription",
					"text": "Different Subscription"
				}
			],
			"required": false
		},
        {
			"id": "4",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the destination resource group?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "5",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "What resource(s) are you trying to move?",
			"watermarkText": "...",
			"required": false
		},
        {
			"id": "6",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Do any of the apps have SSL certificates configured? If yes, are they custom SSL certificates or Azure App Service Certificates?",
			"watermarkText": "...",
			"required": false
		}
    ],
    "$schema": "SelfHelpContent"
}
---