<properties
    pageTitle="Replication"
    description="Replication"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639992, 32780914, 32780920"
    productPesIds="16222,17067,17069"
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
            "id": "is_replica_enabled",
            "order": 3,
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
            "order": 4,
            "visibility": "is_replica_enabled == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your master server?",
            "required": false
        },
        {
            "id": "replica_name",
            "order": 5,
            "visibility": "is_replica_enabled == Yes",
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your replica server?",
            "required": false
        },
        {
            "id": "issue_type",
            "order": 6,
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
            "order": 7,
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
            "order": 8,
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
            "order": 9,
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
            "order": 10,
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
