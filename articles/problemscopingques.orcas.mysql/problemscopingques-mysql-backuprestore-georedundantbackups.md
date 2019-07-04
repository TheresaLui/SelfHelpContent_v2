<properties
    pageTitle="Database Backup Restore"
    description="Database Backup Restore"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640059"
    productPesIds="16221"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-mysql-backuprestore-georedundant_backups"
/>
# Backup, Restore and Business Continuity - Geo redundant backups
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Geo Redundant Backups",
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
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "geo_redundant_enable",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the geo-redundant backup option enabled on the source server?",
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
                    "value": "I don't have the answer",
                    "text": "I don't have the answer"
                }
            ],
            "required": false
        },
        {
            "id": "restore_failures",
            "order": 4,
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
                    "value": "I don't have the answer",
                    "text": "I don't have the answer"
                }
            ],
            "required": false
        },
        {
            "id": "source_server_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the source server name?",
            "required": false
        },
        {
            "id": "target_server_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the target server name?",
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
                },
                {
                    "value": "I don't have the answer",
                    "text": "I don't have the answer"
                }
            ],
            "required": false
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
