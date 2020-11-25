<properties
    pageTitle="Database Backup Restore"
    description="Database Backup Restore"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640015, 32780975, 32780985"
    productPesIds="16222,17067,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-backuprestore-recoverdroppedresource"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Backup, Restore and Business Continuity - Recover A Dropped Resource
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Recover Dropped Resource",
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
            "id": "subscription_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is your subscription ID?",
            "required": false
        },
        {
            "id": "resource_group_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the resource group name of the dropped server?",
            "required": false
        },
        {
            "id": "dropped_server_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the server name of the dropped server?",
            "required": false
        },
        {
            "id": "drop_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did you drop the server? ",
            "required": true
        },
        {
            "id": "guarantee_recovered",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "There is no guarantee the data can be recovered to latest point. Do you accept?",
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
