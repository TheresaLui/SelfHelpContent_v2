<properties
    pageTitle="Database Backup Restore"
    description="Database Backup Restore"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747637"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-flexsvr-backuprestore-dump_issues"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Backup, Restore and Business Continuity - Server dump issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Backup, Restore and Business Continuity",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "dump_request_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did you submit the restore request?",
            "required": true
        },
        {
            "id": "dump_tool",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the tool you used for dump",
            "required": true
        },
        {
            "id": "error_msg",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the error message if you saw",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
