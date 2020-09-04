<properties
	articleId="problemscopingques-sqlmi-conn-config-expressroute"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to Express Route"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32746113"
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
            "id": "source_details",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details about the source",
            "watermarkText": "Please provide details about the network configuration",
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