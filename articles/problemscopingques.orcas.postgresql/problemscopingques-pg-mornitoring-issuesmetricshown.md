<properties
    pageTitle="Monitoring and Alerting"
    description="Monitoring and Alerting"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639994, 32780880, 32780885"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-mornitoring-issuesmetricshown"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Monitoring and Alerting - Issues with metrics shown in the portal
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Monitoring Issues with metrics",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Monitoring and Alerting Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Monitoring and Alerting Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "metrics_issue",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which metric(s) are you experiencing issues viewing?",
            "required": false
        },
        {
            "id": "experience_same_issue",
            "order": 4,
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
            "order": 5,
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
