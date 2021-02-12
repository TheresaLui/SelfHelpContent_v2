<properties
	articleId="problemscopingques-sqlmi-scaling"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture scaling issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637303,32637304"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
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
            "id": "operations",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "What operation(s) are you facing issues with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Changing number of vCores",
                    "text": "Changing number of vCores"
                },
                {
                    "value": "Changing storage size",
                    "text": "Changing storage size"
                },
                {
                    "value": "Changing service tier",
                    "text": "Changing service tier"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message (if any) are you getting?",
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