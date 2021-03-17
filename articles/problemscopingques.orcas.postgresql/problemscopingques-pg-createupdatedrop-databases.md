<properties
    pageTitle="Create Update Drop Resources"
    description="Create Update Drop Resources"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32684527, 32780990, 32780991"
    productPesIds="16222,17067,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-createupdatedrop-databases"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Create Update and Drop Resources - Databases
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Create Update Drop Resources Databases",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Create Update Drop Resources Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Create Update Drop Resources Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "create_method",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you tring to create database from ARM template, Azure CLI or REST API?",
            "infoBalloonText": "Following options are the only supported paths for database creation",
            "dropdownOptions": [
                {
                    "value": "ARM",
                    "text": "ARM template"
                },
                {
                    "value": "CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "dont_know_answer",
                    "text": "REST API"
                }
            ],
            "required": true
        },
        {
            "id": "arm_template",
            "order": 4,
            "controlType": "dropdown",
            "visibility": "create_method == ARM",
            "displayLabel": "Are you creating databases together with your database server?",
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
            "id": "arm_template_content",
            "order": 5,
            "visibility": "create_method == ARM",
            "controlType": "multilinetextbox",
            "displayLabel": "Please Provide the database (not server) resource section in your ARM template:",
            "required": false
        },
        {
            "id": "rest_api",
            "order": 6,
            "visibility": "create_method == dont_know_answer",
            "controlType": "multilinetextbox",
            "displayLabel": "Please Provide the Request Body of your API call:",
            "required": false
        },
        {
            "id": "error",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message you received?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
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