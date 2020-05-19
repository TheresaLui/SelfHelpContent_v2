<properties
	pageTitle="Create a bot channel registration"
	description="Scoping questions to capture more details about issues encountered while creating a bot channel registration"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688635"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="2750A106-78C7-4B04-9C1D-379E5AE478D2"
	ownershipId="Compute_BotService"
/>
# Create a bot channel registration
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Create a bot channel registration",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
		{
			"id": "error_advice",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you seeing an error while creating the registration or are you looking for advice?",
			"radioButtonOptions": [{
					"value": "Error",
					"text": "Seeing an error"
				}, {
					"value": "Advice",
					"text": "Looking for advice"
				}
			],
			"required": true
		},
		{
			"id": "error_desc",
			"order": 4,
			"visibility":"error_advice == Error",
			"controlType": "multilinetextbox",
			"displayLabel": "Please enter the error you see while creating the registration",
			"required": true
		},
		{
			"id": "error_bothandle",
			"order": 5,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Enter the Bot handle you used ",
			"required": false
		},
		{
			"id": "error_subscription",
			"order": 6,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Enter the subscription you used",
			"required": false
		},
		{
			"id": "error_rg",
			"order": 7,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Enter the name of the resource group",
			"required": false
		},
		{
			"id": "error_location",
			"order": 8,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Enter the location you selected",
			"required": false
		},
		{
			"id": "error_pricing",
			"order": 9,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Enter the pricing tier you selected",
			"required": false
		},
		{
			"id": "error_endpoint",
			"order": 10,
			"visibility":"error_advice == Error",
			"controlType": "textbox",
			"displayLabel": "Enter the messaging endpoint URL",
			"required": false
		},
		{
			"id": "error_appins",
			"order": 11,
			"visibility":"error_advice == Error",
			"controlType": "radioButtonGroup",
			"displayLabel": "Do you need App Insights?",
			"radioButtonOptions": [{
					"value": "error_yes",
					"text": "Yes"
				}, {
					"value": "error_no",
					"text": "No"
				}
			],
			"required": false
		},
		{
			"id": "error_appinsloc",
			"order": 12,
			"visibility":"error_appins == Yes",
			"controlType": "textbox",
			"displayLabel": "Enter the selected location for Application Insights",
			"required": false
		},
		{
			"id": "advice_text",
			"order": 13,
			"visibility":"error_advice == Advice",
			"controlType": "multilinetextbox",
			"displayLabel": "Please enter the query you have",
			"required": true
		},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details, if you see an error message list it or you are looking for specific guidance.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible"
        }
	]
}
---
