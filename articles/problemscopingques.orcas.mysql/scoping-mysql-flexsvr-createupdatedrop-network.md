<properties
    pageTitle="Create Update Drop Resources"
    description="Create Update Drop Resources"
	authors="Hang-Zhang"
	ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747628"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-flexsvr-createupdatedrop-network"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Create Update and Drop Resources - Network
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Create Update Drop Resources Network",
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
            "id": "create_method",
            "order": 2,
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
            "order": 3,
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
            "order": 4,
            "visibility": "create_method == ARM",
            "controlType": "multilinetextbox",
            "displayLabel": "Please Provide the database (not server) resource section in your ARM template:",
            "required": false
        },
        {
            "id": "rest_api",
            "order": 5,
            "visibility": "create_method == dont_know_answer",
            "controlType": "multilinetextbox",
            "displayLabel": "Please Provide the Request Body of your API call:",
            "required": false
        },
        {
            "id": "error",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message you received?",
            "required": false
        },
        {
            "id": "resource",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What network resource did you try to create, update or drop?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
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