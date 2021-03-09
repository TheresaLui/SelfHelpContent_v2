<properties
    pageTitle="Database Extensions"
    description="Database Extensions"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639990, 32780848, 32780853"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-extension-issues"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Extensions - Issues with extensions
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Extensions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL DataBase Extensions Troubleshooter",
        "description": "Our Azure Database for PostgreSQL DataBase Extensions Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "extension_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the name of the extension?",
            "required": true
        },
        {
            "id": "extension_version",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the version of the extension?",
            "required": false
        },
        {
            "id": "operation",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What operation do you want to perform?",
            "dropdownOptions": [
                {
                    "value": "Enable",
                    "text": "Enable"
                },
                {
                    "value": "Disable",
                    "text": "Disable"
                }
            ],
            "required": false
        },
        {
            "id": "error",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message that you are getting?",
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
