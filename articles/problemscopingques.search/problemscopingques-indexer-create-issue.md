<properties
	pageTitle="Issue creating an indexer"
	description="Issue creating an indexer"
	authors="dereklegenzoff"
	ms.author="delegenz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681357"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="7c997571-d0da-43c9-a646-701640015e96"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue creating an indexer
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue creating an indexer",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the error you received and any additional information you'd like to share.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "indexer_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name of the indexer you tried to create?",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "interface",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How are you creating the indexer?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "azure_portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "rest_api",
                    "text": "REST API"
                },
                {
                    "value": "sdk",
                    "text": "Azure SDK (C#, Java, Javascript, Python)"
                },
                {
                    "value": "other_answer",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "data_source_firewall",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is your data source behind a firewall or private endpoint?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "firewall",
                    "text": "Firewall"
                },
                {
                    "value": "private_endpoint",
                    "text": "Private Endpoint"
                },
                {
                    "value": "neither",
                    "text": "Neither"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to create the indexer?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---