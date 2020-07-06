<properties
	pageTitle="Cards"
	description="Scoping questions to capture more details about Cards "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688625"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="6DE36ED7-4F74-4AAF-AF8B-45C3D0A80E64"
	ownershipId="Compute_BotService"
/>
# Cards 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cards ",
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
					"text": "Need advice on how to use Cards in a bot"
				}, {
					"value": "3b",
					"text": "Issue implementing cards in a bot"
				}
			],
			"required": true
		},
		{
			"id": "version",
			"order": 4,
			"controlType": "radioButtonGroup",
			"displayLabel": "What is the version of the Bot Framework SDK ?",
			"radioButtonOptions": [{
					"value": "4a",
					"text": "Version 3"
				}, {
					"value": "4b",
					"text": "Version 4"
				}
			],
			"infoBalloonText": "Check the version of Microsoft.Bot.Builder version used by your bot application. If it is 4.x.x, it is using SDK v4, and if it is 3.x.x, it is using SDK v3",
			"required": true
		},
		{
			"id": "card",
			"order": 5,
			"controlType": "multiselectdropdown",
			"displayLabel": "What kind of card are you are using in the bot?",
			"dropdownOptions": [{
					"value": "5a",
					"text": "Adaptive Cards"
				}, {
					"value": "5b",
					"text": "Hero Cards"
				}, {
					"value": "5c",
					"text": "List Card"
				}, {
					"value": "5d",
					"text": "Sign-in Card"
				}, {
					"value": "5e",
					"text": "Thumbnail Card"
				}, {
					"value": "5f",
					"text": "Office 365 Connector Card"
				}
				, {
					"value": "5g",
					"text": "Receipt Card"
				}
				, {
					"value": "5h",
					"text": "Others"
				}
				, {
					"value": "dont_know_answer",
					"text": "Don't know"
				}
			],
			"required": true
		},
		{
			"id": "channel",
			"order": 6,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you facing the issue for a specific channel or for all channels?",
			"radioButtonOptions": [{
					"value": "6a",
					"text": "A specific channel"
				}, {
					"value": "6b",
					"text": "Multiple channels"
				}, {
					"value": "6c",
					"text": "All channels"
				}
			],
			visibility: "kindofassistance == 3b",
			"required": true
		},
		{
			"id": "allusers",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Is the issue impacting a single user or more than one?",
			"dropdownOptions": [{
					"value": "7a",
					"text": "Only seen by me"
				}, {
					"value": "7b",
					"text": "Seen by everyone"
				}
				, {
					"value": "7c",
					"text": "Seen only by users of my organization, not by external users"
				}
				, {
					"value": "7d",
					"text": "Not tested with multiple users"
				}
				, {
					"value": "dont_know_answer",
					"text": "Don't know"
				}
			],
			visibility: "kindofassistance == 3b",
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
