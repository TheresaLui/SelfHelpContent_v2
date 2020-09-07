<properties
    pageTitle="Replication"
    description="Replication"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639976"
    productPesIds="17067,17069,17068"
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
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "enabled_disable",
            "order": 2,
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
            "order": 3,
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
            "order": 4,
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
            "order": 5,
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
            "order": 6,
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
