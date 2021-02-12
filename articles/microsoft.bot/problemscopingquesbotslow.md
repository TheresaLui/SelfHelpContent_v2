<properties
	pageTitle="Bot is slow to respond"
	description="Scoping questions to capture more details about issues encountered while connecting or interacting with a bot"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32689883"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="631FA214-FF21-4827-B678-AD2B49436F2C"
	ownershipId="Compute_BotService"
/>
# Bot is slow to respond
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Bot is slow to respond",
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
            "id": "time_text",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "How long did it take for the bot to respond?",
            "watermarkText": "enter value in seconds"
        },
        {
            "id": "intermittent_dropdown",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "How frequent is the issue?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose one",
            "dropdownOptions": [
                {
                    "value": "NotIntermittent_All",
                    "text": "All the time"
                },
                {
                    "value": "NotIntermittent_Most",
                    "text": "Most of the time"
                },
                {
                    "value": "NotIntermittent_Once",
                    "text": "Once in a while"
                }
			],
			"required": false
        },
        {
            "id": "peak_dropdown",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does the issue happen only during peak hours?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose one",
            "dropdownOptions": [
                {
                    "value": "Peak_Yes",
                    "text": "Yes"
                },
                {
                    "value": "Peak_No",
                    "text": "No"
                }
			],
			"required": false
        },
        {
            "id": "channel_dropdown",
            "order": 9,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which channel(s) are you seeing the issue?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "For errors encountered during creating or deploying a bot or during configuration, or when the bot works on some channels and fails on others,  please go back and select the appropriate categories",
            "dropdownOptions": [
                {
                    "value": "channel_all",
                    "text": "All channels"
                },
                {
                    "value": "channel_1",
                    "text": "Direct Line"
                },
                {
                    "value": "channel_2",
                    "text": "Web Chat"
                },
                {
                    "value": "channel_3",
                    "text": "Teams"
                },
				{
                    "value": "channel_4",
                    "text": "Cortana"
                },
				{
                    "value": "channel_5",
                    "text": "Email"
                },
				{
                    "value": "channel_6",
                    "text": "Facebook"
                },
				{
                    "value": "channel_7",
                    "text": "Kik"
                },
				{
                    "value": "channel_8",
                    "text": "Skype"
                },
				{
                    "value": "channel_9",
                    "text": "Skype for Business"
                },
				{
                    "value": "channel_9",
                    "text": "LINE"
                },
				{
                    "value": "channel_10",
                    "text": "Slack"
                },
				{
                    "value": "channel_11",
                    "text": "Telegram"
                },
				{
                    "value": "channel_12",
                    "text": "Twilio"
                },
				{
                    "value": "channel_13",
                    "text": "WeChat"
                },
                {
                    "value": "channel_other",
                    "text": "Other error not listed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
	    {
            "id": "sdk_dropdown",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What version of SDK is the bot running on?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the version of SDK",
            "dropdownOptions": [
                {
                    "value": "sdk_v3",
                    "text": "Version 3"
                },
                {
                    "value": "sdk_v4",
                    "text": "Version 4"
                },
				{
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
			],
			"required": true
        },
		{
            "id": "language_dropdown",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "What language of SDK are you using?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the language of SDK",
            "dropdownOptions": [
                {
                    "value": "language_C#",
                    "text": "C#"
                },
                {
                    "value": "language_JS",
                    "text": "Node.js"
                },
				{
                    "value": "language_Python",
                    "text": "Python"
                },
				{
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
			],
			"required": true
        },
		{
            "id": "howcreated_dropdown",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "How did you create the bot?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the method you used to create the bot",
            "dropdownOptions": [
                {
                    "value": "howcreated_Portal",
                    "text": "Azure Portal Template"
                },
                {
                    "value": "howcreated_SDK",
                    "text": "Bot Framework SDK"
                },
				{
                    "value": "howcreated_other",
                    "text": "Other"
                }
			],
			"required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full description of the issue you are encountering."
        }
	]
}
---
