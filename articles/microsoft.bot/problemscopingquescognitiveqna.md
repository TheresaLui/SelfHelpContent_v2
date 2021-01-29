<properties
	pageTitle="Cognitive - QnA Maker"
	description="Scoping questions to capture more details about Cognitive - QnA Maker "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688629"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="A0C15CEA-8E1D-4252-8467-337F49AAE779"
	ownershipId="Compute_BotService"
/>
# Cognitive - QnA Maker 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cognitive - QnA Maker ",
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
			"id": "kindofassistance",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "What kind of help do you need?",
			"radioButtonOptions": [{
					"value": "3a",
					"text": "Need advice on how to use QnA maker with a bot"
				}, {
					"value": "3b",
					"text": "Seeing an issue when using QnA maker with a bot"
				}
			],
			"required": true
		},
		{
			"id": "work",
			"order": 4,
			"controlType": "radioButtonGroup",
			"displayLabel": "Does the knowledge base work correctly (correct answers/correct format) when testing it in the QnA portal? ",
			"radioButtonOptions": [{
					"value": "4a",
					"text": "Yes"
				}, {
					"value": "4b",
					"text": "No"
				}
			],
			"visibility": "kindofassistance == 3b",
			"required": true
		},
		{
			"id": "channel",
			"order": 5,
			"controlType": "radioButtonGroup",
			"displayLabel": "When you are calling the QnA maker from bot, is it failing for a specific channel or for all channels?",
			"radioButtonOptions": [{
					"value": "5a",
					"text": "A specific channel"
				}, {
					"value": "5b",
					"text": "Multiple channels"
				}, {
					"value": "5c",
					"text": "All channels"
				}
			],
			"visibility": "kindofassistance == 3b",
			"required": true
		},
		{
			"id": "multiturn",
			"order": 6,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you having a trouble only with multi-turn conversation?",
			"radioButtonOptions": [{
					"value": "6a",
					"text": "Yes"
				}, {
					"value": "6b",
					"text": "No"
				}
			],
			"visibility": "kindofassistance == 3b",
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
