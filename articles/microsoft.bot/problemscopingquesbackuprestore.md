<properties
	pageTitle="Back up or restore a bot"
	description="Scoping questions to capture more details about back up or restore a bot"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688658"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="BB26A879-11C9-4529-A772-70896E6C2655"
	ownershipId="Compute_BotService"
/>
# Back up or restore a bot
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Back up or restore a bot",
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
			"displayLabel": "Which of the following you need help with?",
			"radioButtonOptions": [
			    {
					"value": "backupg",
					"text": "Guidance for creating a backup for my Bot"
				},
				{
					"value": "restoreg",
					"text": "Guidance for restoring a backup for my Bot"
				},
				{
					"value": "backupe",
					"text": "Running into an issue while creating a backup for my Bot"
				},
				{
					"value": "restoree",
					"text": "Running into an issue while restoring a backup for my Bot"
				},
				{
					"value": "advice",
					"text": "What are the best practices for backing up and restoring a Bot"
				},
				{
					"value": "Other",
					"text": "Need help with something else"
				}
			],
			"required": true
		},
		{
			"id": "backup_details",
			"order": 4,
			"visibility":"error_advice == restoreg || error_advice == restoree",
			"controlType": "radioButtonGroup",
			"displayLabel": "If you are trying to restore from an existing backup, how was the backup created?",
			"radioButtonOptions": [
			    {
					"value": "bac_azure",
					"text": "Backup created on Azure"
				},
				{
					"value": "bac_marketplace",
					"text": "An application from Azure Marketplace"
				},
				{
					"value": "bac_others",
					"text": "Something else"
				}
			],
			"required": true
		},
		{
			"id": "intermittent",
			"order": 5,
			"visibility":"error_advice == restoree || error_advice == backupe",
			"controlType": "radioButtonGroup",
			"displayLabel": "Can you reproduce the issue at will?",
			"radioButtonOptions": [
			    {
					"value": "int_yes",
					"text": "Yes"
				},
				{
					"value": "int_no",
					"text": "No"
				}
			],
			"required": true
		},
		{
			"id": "allusers",
			"order": 6,
			"visibility":"error_advice == restoree || error_advice == backupe",
			"controlType": "radioButtonGroup",
			"displayLabel": "Does the issue happen to all users",
			"radioButtonOptions": [
			    {
					"value": "all_yes",
					"text": "Yes"
				},
				{
					"value": "all_no",
					"text": "No"
				}
			],
			"required": true
		},
		{
            "id": "troubleshooting",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "If you have followed an guidance or troubleshooting steps, please provide a summary of the details below",
            "watermarkText": "Please provide as much details as possible"
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
