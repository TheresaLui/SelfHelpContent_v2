<properties
	pageTitle="CosmosDB Backup and Restore Info"
	description="CosmosDB Backup and Restore Info"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32741531,32636825,32748845"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="a7dc710a-d040-4c21-9ab6-53c85567d58e"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Backup and restore Info
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Backup and Restore Info",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
		{
            "id": "request_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the reason for the support request?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Restore of deleted or corrupted data",
                    "text": "Restore of deleted or corrupted data"
                },
                {
                    "value": "Update backup policy",
                    "text": "Update backup policy"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Non restore request"
                }
            ],
            "required": true
        },
        {
            "id": "sourceaccount_name",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Name of the database account to restore",
			"required": true
        },
		{
            "id": "restore_point",
            "order": 4,
			"visibility": "request_type == Restore of deleted or corrupted data",
			"controlType": "datetimepicker",
			"displayLabel": "Restore point of your data (Required)",
			"infoBalloonText": "Please enter your desired restore point in your local time, we will retrieve the closest backup we have to this time. This form will automatically convert your entered time value to UTC when submitted.",
			"required": true
        },
		{
            "id": "restore_all",
            "order": 5,
			"visibility": "request_type == Restore of deleted or corrupted data",
            "controlType": "dropdown",
            "displayLabel": "Restore all databases and collections under your account?",
            "watermarkText": "Choose an option",
			"infoBalloonText": "If you want only specific databases or collections restored then select no. If you want everything under your account restored back to a restore point then select yes.",
            "dropdownOptions": [
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "database_name",
			"order": 6,
			"visibility": "restore_all == No",
			"controlType": "textbox",
			"displayLabel": "Database to restore",
			"required": true
        },
        {
            "id": "collection_name",
			"order": 7,
			"visibility": "restore_all == No",
			"controlType": "textbox",
			"displayLabel": "Collections to restore (semicolon separated)",
			"required": false
        },
		{
            "id": "backup_interval",
			"visibility": "request_type == Update backup policy",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "How often would you like your backups to be performed? (hours)",
            "required": true
        },
		{
            "id": "backup_retention",
			"visibility": "request_type == Update backup policy",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "How long would you like your backups to be saved? (hours)",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the restore request.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
