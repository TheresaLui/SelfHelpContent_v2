<properties
    pageTitle="Server Parameters"
    description="Server Parameters"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639997, 32780952, 32780956"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-server-modifyparameters"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Server Parameters - Modify server parameters
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Server Parameters Modify",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Server Parameters Troubleshooter",
        "description": "Our Azure Database for Server Parameters Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "server_parameter",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What server parameter(s) do you want to change?",
            "required": false
        },
        {
            "id": "parameter_value",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the value you want to change the parameter to?",
            "required": false
        },
        {
            "id": "error_message",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message you received?",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 6,
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
