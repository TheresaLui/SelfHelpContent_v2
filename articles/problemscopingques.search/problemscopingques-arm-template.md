<properties
	pageTitle="Issue using the ARM template"
	description="Issue using the ARM template"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681372"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="d9da78f1-e7af-4481-92a4-cec1f1384e8b"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue using the ARM template
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue using the ARM template",
    "fileAttachmentHint": "Please attach a copy of the ARM template used.",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe what issue you experienced",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error text when possible."
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "operation",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What operation are you trying to perform?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create a new search service",
                    "text": "Create a new search service"
                },
                {
                    "value": "Scale a search service up or down",
                    "text": "Scale a search service up or down"
                },
                {
                    "value": "Modify an existing search service",
                    "text": "Modify an existing search service"
                },
                {
                    "value": "Permanently delete a search service",
                    "text": "Permanently delete a search service"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
