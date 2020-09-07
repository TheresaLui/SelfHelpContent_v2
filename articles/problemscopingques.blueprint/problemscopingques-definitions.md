<properties
	articleId="problemscopingques-definitions.md"
	pageTitle="Azure Blueprint - Blueprint Definitions"
	description="Azure Blueprint - Blueprint Definitions"
	authors="apclouds"
	ms.author="angperez"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739602,32739607,32739605,32739609"
	productPesIds="16600"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AzureBlueprint"
/>
# Blueprint Definitions
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Blueprint Definition",
    "fileAttachmentHint": "Please provide a screenshot of any errors",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "blueprint_definition_name",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide the exact name of your blueprint definition",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include the exact text of any error messages that occur"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
