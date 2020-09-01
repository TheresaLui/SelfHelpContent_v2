<properties
	articleId="dw-scoping-backuprestoreandbusinesscontinuity-restoringfrombackup.md"
	pageTitle="Restoring from backup"
	description="Restoring from backup"
	authors="mlee3gsd"
	ms.author="martinle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635218"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Backup, Restore and Business Continuity - Restoring from backup
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Restoring from backup",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the maintenance occur?",
            "required": true
        },
        {
            "id": "dw_scoping_backup_backupregion",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What region is your backup located?",
            "required": false
        },
        {
            "id": "dw_scoping_backup_restoreregion",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the region you are restoring to?",
            "required": false
        },
        {
            "id": "dw_scoping_backup_error",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "If an error was displayed, what was the error message?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---