<properties
    pageTitle="Security"
    description="Security"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32740814, 32780942, 32780950"
    productPesIds="16222,17067,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-security-dataencryption"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Security - Data Encryption
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Security Data Encryption",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Security Troubleshooter",
        "description": "Our Azure Database for Security Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "error",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "If an error was displayed, what was the error message (including operation ID from activity log, if any)?",
            "required": false
        },
        {
            "id": "issue",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the specific issue you are facing?",
            "dropdownOptions": [
                {
                    "value": "Issues with key vault during Initial Setup",
                    "text": "Issues with key vault during Initial Setup"
                },
                {
                    "value": "Database is in an inaccessible State",
                    "text": "Database is in an inaccessible State"
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