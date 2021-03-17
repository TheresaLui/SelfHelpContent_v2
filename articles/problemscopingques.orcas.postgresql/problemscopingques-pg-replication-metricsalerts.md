<properties
    pageTitle="Replication"
    description="Replication"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639995, 32780915, 32780921"
    productPesIds="16222,17067,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-replication-metricsalerts"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Replication - Metrics and alerts
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Replication Metrics and alerts",
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
            "id": "master_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is your master server name?",
            "required": false
        },
        {
            "id": "replica_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is your replica server name?",
            "required": false
        },
        {
            "id": "metrics_experience",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Which metric(s) are you experiencing issues with?",
            "required": false
        },
        {
            "id": "same_issue_servers",
            "order": 6,
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
            "order": 7,
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
