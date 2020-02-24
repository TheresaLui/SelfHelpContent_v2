<properties
	pageTitle="CosmosDB Backup and Restore Info"
	description="CosmosDB Backup and Restore Info"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636805,32636825"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	schemaVersion="1"
	articleId="a7dc710a-d040-4c21-9ab6-53c85567d58e"
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
                    "value": "Restore of a database or collection",
                    "text": "Restore of a database or collection"
                },
                {
                    "value": "Backup retention policy",
                    "text": "Backup retention policy"
                },
                {
                    "value": "Backup frequency",
                    "text": "Backup frequency"
                },
                {
                    "value": "Non restore request",
                    "text": "Non restore request"
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
			"order": 4,
			"visibility": "request_type == Restore a database or collection",
			"controlType": "textbox",
			"displayLabel": "Database to restore",
			"required": true
        },
        {
            "id": "collection_name",
			"order": 5,
			"visibility": "request_type == Restore a database or collection",
			"controlType": "textbox",
			"displayLabel": "Collections to restore (semicolon separated)",
			"required": true
        },
		{
            "id": "restore_point",
            "order": 6,
			"visibility": "request_type == Restore a database or collection",
			"controlType": "datetimepicker",
			"displayLabel": "Restore point",
			"infoBalloonText": "Please enter your desired restore point in your local time. This form will automatically convert your entered time value to UTC when submitted.",
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
