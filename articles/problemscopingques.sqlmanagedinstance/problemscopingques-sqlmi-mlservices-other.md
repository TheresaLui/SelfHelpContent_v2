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
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Instance",
    "fileAttachmentHint": "",
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
                "defaultDropdownOptions": {
                    "value": "Yes",
                    "text": "Yes"
                }
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
            "required": true
        },
        {
            "id": "instances",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "What's the Managed Instance(s) you wish to enable ML Services?",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/managedInstances?api-version=2018-06-01-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of instances",
                    "text": "Unable to get the list of instances"
                }
            ],
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
