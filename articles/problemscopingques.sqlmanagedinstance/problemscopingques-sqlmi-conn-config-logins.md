<properties
	articleId="problemscopingques-sqlmi-conn-config-logins"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture driver related issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32745433,32746114"
    productPesIds="13491,16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "SQL Database Managed Instance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "method",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Authentication method you are experiencing issues with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "SQL Authentication",
                    "text": "SQL Authentication"
                },
                {
                    "value": "Azure Active Directory Authentication",
                    "text": "Azure Active Directory Authentication"
                },
                {
                    "text": "Don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "sqlexception_received_on_client",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Paste detailed error message or stack trace. (Remove any personally identifiable information).",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
