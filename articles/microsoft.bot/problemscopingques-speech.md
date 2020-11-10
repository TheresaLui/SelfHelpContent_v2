<properties
	pageTitle="Cognitive Speech"
	description="Scoping questions to capture more details about Cognitive - Speech "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688630"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="6A19994B-AC4D-44BA-B96F-FFB44B25B2CD"
	ownershipId="Compute_BotService"
/>
# Cognitive - Speech 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cognitive - Speech ",
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
			"displayLabel": "Are you using the Direct Line Speech or Speech SDK? ",
			"radioButtonOptions": [{
					"value": "3a",
					"text": "Direct Line Speech"
				}, {
					"value": "3b",
					"text": "Speech SDK"
				}
			],
			"required": true
		},
		{
			"id": "advice",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What do you need help on?",
			"dropdownOptions": [{
					"value": "5a",
					"text": "Configuring Direct Line Speech channel"
				}, {
					"value": "5b",
					"text": "Speech to Text"
				}, {
					"value": "5c",
					"text": "Text to Speech"
				},
				{
					"value": "dont_know_answer",
					"text": "Don't know"
				}
			],
			"required": true
		},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details, if you see an error message list it or you are looking for specific guidance. Provide steps to repro as well.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible"
        }
	]
}
---
