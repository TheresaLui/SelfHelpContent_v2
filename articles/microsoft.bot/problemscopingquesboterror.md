<properties
	pageTitle="Bot is returning an error"
	description="Scoping questions to capture more details about errors encountered while connecting or interacting with a bot"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688623"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="E0099F57-8791-4D2D-AB5C-5FE7B97597BA"
	ownershipId="Compute_BotService"
/>
# Bot is returning an error
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Bot is returning an error",
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
            "id": "error_dropdown",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What error are you seeing?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "For errors encountered during creating or deploying a bot or during configuration, or when the bot works on some channels and fails on others,  please go back and select the appropriate categories",
            "dropdownOptions": [
                {
                    "value": "Error_Sending_Message",
                    "text": "There was an error sending this message to your bot"
                },
                {
                    "value": "Error_Code_Issue",
                    "text": "Sorry my bot code is having an issue"
                },
                {
                    "value": "Error_401",
                    "text": "HTTP 401 Error"
                },
				{
                    "value": "Error_403",
                    "text": "HTTP 403 Error"
                },
				{
                    "value": "Error_404",
                    "text": "HTTP 404 Error"
                },
				{
                    "value": "Error_405",
                    "text": "HTTP 405 Error"
                },
				{
                    "value": "Error_409",
                    "text": "HTTP 409 Error"
                },
				{
                    "value": "Error_412",
                    "text": "HTTP 412 Error"
                },
				{
                    "value": "Error_429",
                    "text": "HTTP 429 Error"
                },
				{
                    "value": "Error_500",
                    "text": "HTTP 500 Error"
                },
				{
                    "value": "Error_502",
                    "text": "HTTP 502 Error"
                },
				{
                    "value": "Error_503",
                    "text": "HTTP 503 Error"
                },
                {
                    "value": "Error_Other",
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
            "id": "channel_dropdown",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which channel(s) are you seeing the issue?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select the channel(s) that you see the issue with. You can select multiple channels or select all channels if the issue is occuring regardless of the channel",
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
                    "text": "Other channel(s)"
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
                }
		],
		"required": false
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
            "id": "intermittent_dropdown",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Is the issue reproducible at will or occuring all the time?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose No if you can't reproduce the issue at will",
            "dropdownOptions": [
                {
                    "value": "NotIntermittent_Yes",
                    "text": "Yes"
                },
                {
                    "value": "NotIntermittent_No",
                    "text": "No"
                }
			],
			"required": false
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
            "watermarkText": "Please provide the full error text that you are encountering."
        }
	]
}
---
