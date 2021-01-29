<properties
	pageTitle="cConnector or REST API"
	description="Scoping questions to capture more details about Connector or REST API "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688633"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="568A90D8-0AA5-4969-BB75-694107839D9A"
	ownershipId="Compute_BotService"
/>
# Connector or REST API 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Connector or REST API ",
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
			"id": "mode",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you using the Bot Framework SDK or the REST API? ",
			"radioButtonOptions": [{
					"value": "3a",
					"text": "Bot Framework SDK"
				}, {
					"value": "3b",
					"text": "REST API"
				}
			],
			"required": true
		},
		{
			"id": "advice",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Which SDK are you making use of?",
			"dropdownOptions": [{
					"value": "5a",
					"text": "C#"
				}, {
					"value": "5b",
					"text": "JavaScript"
				}, {
					"value": "5c",
					"text": "Python"
				},
				{
					"value": "dont_know_answer",
					"text": "Don't know"
				}
			],
			"visibility": "mode == 3a",
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
