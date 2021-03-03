<properties
    pageTitle="Replication"
    description="Replication"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639976, 32780919"
    productPesIds="16222,17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-replication-enabledisable"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Replication - Enable or disable replication support for PG
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Enable or disable replication support",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Replication Troubleshooter",
        "description": "Our Azure Database for Replication Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "enabled_disable",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to enable or disable replication?",
            "dropdownOptions": [
                {
                    "value": "Enable",
                    "text": "Enable"
                },
                {
                    "value": "Disable",
                    "text": "Disable"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": true
        },
        {
            "id": "enable_button",
            "order": 4,
            "visibility": "enabled_disable == Enable",
            "controlType": "dropdown",
            "displayLabel": "Did you try clicking on the Enable Replication Support button in the portal under Replication section?",
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
            "required": false
        },
        {
            "id": "enable_issue",
            "order": 5,
            "visibility": "enable_button == Yes",
            "controlType": "dropdown",
            "displayLabel": "Are you facing an issue while performing this action?",
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
            "required": false
        },
        {
            "id": "disable_button",
            "order": 6,
            "visibility": "enabled_disable == Disable",
            "controlType": "dropdown",
            "displayLabel": "Did you try clicking on the Disable Replication Support button in the portal under Replication section?",
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
            "required": false
        },
        {
            "id": "disable_issue",
            "order": 7,
            "visibility": "disable_button == Yes",
            "controlType": "dropdown",
            "displayLabel": "Are you facing an issue while performing this action?",
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
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Please provide the repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
