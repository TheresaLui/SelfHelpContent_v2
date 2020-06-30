<properties
	pageTitle="Deploying a bot Using ARM and AZ CLI "
	description="Scoping questions to capture more details about issues encountered while deploying a bot Using ARM and AZ CLI "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688661"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="CCD78FF1-5210-418B-B01E-17264949196F"
	ownershipId="Compute_BotService"
/>
# Deploying a bot Using ARM and AZ CLI 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Deploying a bot Using ARM and AZ CLI ",
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
			"id": "appid",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "Do you already have an App ID registered with Azure Active Directory or you are creating a new one?",
			"radioButtonOptions": [{
					"value": "new",
					"text": "New app"
				}, {
					"value": "existing",
					"text": "Existing app"
				}
			],
			"required": true
		},
		{
            "id": "appidname",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide App ID name",
            "required": true,
			visibility: "appid == existing"
        },
		{
			"id": "rg",
			"order": 5,
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you using existing Resource Group or new Resource Group?",
			"radioButtonOptions": [{
					"value": "new_rg",
					"text": "New Resource Group"
				}, {
					"value": "existing_rg",
					"text": "Existing Resource Group"
				}
			],
			"required": true
		},
		{
            "id": "rgname",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Please provide Resource Group name",
            "required": true,
			visibility: "rg == existing_rg"
        },
		{
			"id": "command",
			"order": 7,
			"controlType": "multilinetextbox",
			"displayLabel": "Please type in the command you are using to deploy the bot ",
			"infoBalloonText": "<a href='https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0&tabs=csharp'>Deploy your bot</a>",
			"watermarkText": "Remove any sensitive information like password/secret",
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
