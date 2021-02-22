<properties
    pageTitle="Database Backup Restore"
    description="Database Backup Restore"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639968, 32780969, 32780979"
    productPesIds="16222,17067,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-backuprestore-automatedbackups"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Backup, Restore and Business Continuity - Automated backups
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Automated Backups",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Backup Restore Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Backup Restore Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Following the steps in Recommended Solution section below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "restore_request_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did you submit the restore request?",
            "required": true
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
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
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
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Please provide the repro steps and other information about your issue.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
