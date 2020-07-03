<properties
	pageTitle="Managing a bot configuration"
	description="Scoping questions to capture more details about issues encountered while Mmanaging a bot configuration"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688652"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="E3702653-E4E0-46E0-8761-C2D60C0FC4B7"
	ownershipId="Compute_BotService"
/>
# Managing a bot configuration
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Managing a bot configuration",
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
			"id": "bot_type",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "What kind of bot configuration do you want to manage?",
			"radioButtonOptions": [{
					"value": "webbot",
					"text": "Web App Bot"
				}, {
					"value": "bcr",
					"text": "Bot Channel Registration"
				}
			],
			"required": true
		},
		{
            "id": "configuration",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "What configuration you need help on?",
			"dropdownOptions": [
                {
                    "value": "1",
                    "text": "Channel"
                },
                {
                    "value": "2",
                    "text": "Authentication"
                },
                {
                    "value": "3",
                    "text": "Application Insights"
                },
				{
                    "value": "4",
                    "text": "Application ID and Password"
                },
                {
                    "value": "5",
                    "text": "Analytics"
                },
				{
                    "value": "6",
                    "text": "Messaging Endpoint"
                },
				{
                    "value": "7",
                    "text": "Bot profile"
                },
				{
                    "value": "8",
                    "text": "Other"
                },
			{
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
	    ],
            "required": true,
	    "watermarkText": "Please select one of the below"
        },
		{
			"id": "other",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Since you selected other, please specify below on what configuration you need help on",
			"visibility":"configuration == 8",
			"required": true
		},
				{
			"id": "error",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Are you seeing any errors while configuring a bot? Please provide us the details",
			"required": false
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
