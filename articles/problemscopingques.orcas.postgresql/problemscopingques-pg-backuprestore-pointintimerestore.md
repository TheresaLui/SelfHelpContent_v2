<properties
    pageTitle="Database Backup Restore"
    description="Database Backup Restore"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640011"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-backuprestore-pointintimerestore"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
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
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "restore_request_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did you submit the restore request?",
            "required": true
        },
        {
            "id": "restore_failures",
            "order": 3,
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "source_server_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the source server name?",
            "required": false
        },
        {
            "id": "target_server_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the target server name?",
            "required": false
        },
        {
            "id": "source_server_createtime",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When was the source server created?",
            "required": false
        },
        {
            "id": "restore_pointin_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "What is the point in time you selected for restore?",
            "required": false
        },
        {
            "id": "restore_request_from",
            "order": 8,
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
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
