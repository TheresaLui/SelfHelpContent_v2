<properties
	pageTitle="Database Backup Restore"
	description="Database Backup Restore"
	authors="Hang-Zhang"
	ms.author="haz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640145"
	productPesIds="16617"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-mariadb-backuprestore-pointintime_restore"
/>
# Backup, Restore and Business Continuity - Point in Time Restore
---
{
	"resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Point in Time Restore",
    "fileAttachmentHint": "",
	"formElements": [
        {
            "id": "restore_request_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did you submit the restore request?",
            "required": true
        },
        {
			"id": "restore_failures",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you encountered any restore failures?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
		{
			"id": "source_server_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the source server name?",
            "required": true
		},
		{
            "id": "target_server_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the target server name?",
            "required": true
        },
        {
            "id": "source_server_createtime",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When was the source server created?",
            "required": false
        },
        {
            "id": "restore_pointin_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "What is the point in time you selected for restore?",
            "required": false
        },
		{
            "id": "restore_request_from",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Did you submit the restore request from the Azure portal or Azure CLI?",
            "dropdownOptions": [
                {
                    "value": "Azure portal",
                    "text": "Azure portal"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                }
            ],
            "required": true
        },
		{
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
	],
	"$schema": "SelfHelpContent"
}
---
