<properties
    pageTitle="Replication"
    description="Replication"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639992"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-replication-issues"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Replication - Issues to Azure Database for PG
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issues with Replication",
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
            "id": "is_replica_enabled",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have a replication that is already enabled?",
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
            "required": true
        },
        {
            "id": "master_name",
            "order": 3,
            "visibility": "is_replica_enabled == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your master server?",
            "required": false
        },
        {
            "id": "replica_name",
            "order": 4,
            "visibility": "is_replica_enabled == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your replica server?",
            "required": false
        },
        {
            "id": "issue_type",
            "order": 5,
            "visibility": "is_replica_enabled == Yes",
            "controlType": "dropdown",
            "displayLabel": "What issue are you facing with your replica server?",
            "dropdownOptions": [
                {
                    "value": "not_working",
                    "text": "Replication Not Working"
                },
                {
                    "value": "high_latency",
                    "text": "High delay/Latency"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": true
        },
        {
            "id": "multiple_replica",
            "order": 6,
            "visibility": "is_replica_enabled == Yes",
            "controlType": "dropdown",
            "displayLabel": "Do you have more than one replica server?",
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
            "id": "issue_with_all",
            "order": 7,
            "visibility": "multiple_replica == Yes",
            "controlType": "dropdown",
            "displayLabel": "Are you facing issues with all the replica servers?",
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
            "id": "enable_replica",
            "order": 8,
            "visibility": "is_replica_enabled == No",
            "controlType": "dropdown",
            "displayLabel": "Are you facing any issues enabling a replication?",
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
            "required": true
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
