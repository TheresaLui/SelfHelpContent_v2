<properties
	articleId="problemscopingques-sqlmi-mlservices-other"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture instance ML Services issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
   	productPesIds="16259"
	supportTopicIds="32742351"
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
            "id": "enrollment",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to sign up for the Preview?",
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
            "id": "server",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the Managed Instance name(s) you wish to enable ML Services?",
            "required": true,
            "visibility": "enrollment == Yes"
        },
        {
            "id": "region",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What Azure region(s) is your instance(s) in?",
            "required": true,
            "visibility": "enrollment == Yes"
        },
        {
            "id": "subscription",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please confirm your SubscriptionId?",
            "required": true,
            "visibility": "enrollment == Yes"
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your request",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
