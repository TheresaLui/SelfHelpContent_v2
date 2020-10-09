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
            "displayLabel": "Additional details",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "create_error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "interface",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What did you use to create the indexer?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "REST API",
                    "text": "REST API"
                },
                {
                    "value": "Azure SDK (C#, Java, Javascript, Python)",
                    "text": "SDK"
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
            "displayLabel": "Is your data source behind a firewall?",
            "watermarkText": "Choose an option",
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
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "data_source_vnet",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is your data source inside a private network?",
            "watermarkText": "Choose an option",
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
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to delete the service?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---