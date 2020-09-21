<properties
	pageTitle="Deployment via Visual Studio"
	description="Scoping questions to capture more details about Deployment via Visual Studio "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688663"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="20D811C6-2139-4545-926A-8586D81FE536"
	ownershipId="Compute_BotService"
/>
# Deployment via Visual Studio 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Deployment via Visual Studio",
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
			"id": "version",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "What version of the Bot Framework SDK are you using? ",
			"radioButtonOptions": [{
					"value": "3a",
					"text": "Version 3"
				}, {
					"value": "3b",
					"text": "Version 4"
				}
			],
			"infoBalloonText": "Check the version of Microsoft.Bot.Builder version used by your bot application. If it is 4.x.x, it is using SDK v4, and if it is 3.x.x, it is using SDK v3",
			"required": true
		},
		{
			"id": "language",
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
			"required": true
		},
		 {
            "id": "vsversion",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Please provide the version of Visual Studio and extensions that are being used",
            "required": true
        },
		{
			"id": "deploy",
			"order": 4,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you able to deploy using other methods of deployment",
			"radioButtonOptions": [{
					"value": "4a",
					"text": "Yes"
				}, {
					"value": "4b",
					"text": "No"
				}
			],
			"required": true
		},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details, please provide steps to repro as well. Or if you are looking for specific guidance please detail that here.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible including error message, stack trace or troubleshooting steps followed"
        }
	]
}
---
