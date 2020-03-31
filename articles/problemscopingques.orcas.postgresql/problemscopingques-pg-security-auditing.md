<properties
    pageTitle="Security"
    description="Security"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639967"
    productPesIds="16222"
    cloudEnvironments="public, Fairfax"
    schemaVersion="1"
    articleId="problemscopingques-pg-security-auditing"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Security - Auditing
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Security Auditing",
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
            "id": "audit_logging_enable",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you enabled audit logging from the server parameters?",
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
            "id": "sending_log",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Where are you sending the logs to? Event Hubs, Azure Storage, or Log Analytics?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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