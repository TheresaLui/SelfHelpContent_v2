<properties
    pageTitle="Replication"
    description="Replication"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32673563"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax"
    schemaVersion="1"
    articleId="problemscopingques-mariadb-replication-metrics_alerts"
/>
# Replication - Metrics and alerts
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Replication Metrics and alerts",
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
            "id": "master_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is your master server name?",
            "required": false
        },
        {
            "id": "replica_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is your replica server name?",
            "required": false
        },
        {
            "id": "metrics_experience",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which metric(s) are you experiencing issues with?",
            "required": false
        },
        {
            "id": "same_issue_servers",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "If you have multiple servers, did you experience the same issue on other servers?",
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
