<properties
    pageTitle="Database Backup Restore"
    description="Database Backup Restore"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640113"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-mariadb-backuprestore-automated_backups"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Backup, Restore and Business Continuity - Automated backups
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Automated Backups",
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
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the source server name?",
            "required": false
        },
        {
            "id": "target_server_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the target server name?",
            "required": false
        },
        {
            "id": "restore_request_from",
            "order": 5,
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
            "order": 6,
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
