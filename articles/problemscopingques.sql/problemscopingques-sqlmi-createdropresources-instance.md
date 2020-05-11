<properties
	articleId="problemscopingques-sqlmi-createdropresources-instance"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture instance CRUD issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
   	productPesIds="16259"
	supportTopicIds="32637269"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "title": "Instance",
    "fileAttachmentHint": "",
    "subscriptionRequired": false,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controltype": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Specify when the problem started",
            "infoBalloonText": "Specify when the problem started",
            "required": true
        },
        {
            "id": "attempt_method",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What method are you using?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "azure_portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "powershell",
                    "text": "Powershell"
                },
                {
                    "value": "azure_cli",
                    "text": "Azure CLI"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "encountering_an_error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you encountering an error message?",
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
                    "text": "Unsure"
                }
            ],
            "required": false
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the error message",
            "required": false,
            "visibility": "encountering_an_error == Yes"
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
