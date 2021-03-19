<properties
	pageTitle="Search Index/Issue creating an index"
	description="Issue creating an index"
	authors="luisca"
	ms.author="luisca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681356"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="9682b4d2-9f94-4b4b-b386-a90216f42ea1"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue creating an index
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue creating an index",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details. Please provide the exact error you receive.",
            "required": true,
            "useAsAdditionalDetails": true
        },

        {
            "id": "unusual",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Is this a task you have performed in the past? Is this behavior unusual? If you are trying something different, please elaborate.",
            "required": false
        },

        {
            "id": "creation_mechanism",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How are you creating the index?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "REST",
                    "text": "Programmatically, using REST APIs"
                },
                {
                    "value": "SDK",
                    "text": "Programmatically, using SDK"
                },
                {
                    "value": "Portal_Import_Data",
                    "text": "Using the Azure Portal - Import Data Flow"
                },
                {
                    "value": "Portal_Import_Data",
                    "text": "Using the Azure Portal - Creating Index Directly"
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
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did you start seeing the issue?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---