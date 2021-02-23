<properties
	pageTitle="Issue with an built-in cognitive skill"
	description="Issue with an built-in cognitive skill"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681375"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="52d34a05-9aec-4d02-bd9d-95e69e425531"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue with an built-in cognitive skill
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue with an built-in cognitive skill",
    "fileAttachmentHint": "Attach screenshots or logs with details of the error",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the issue you experienced",
            "useAsAdditionalDetails": true,
            "required": true,
	    "watermarkText":"Please provide the full error text when possible."
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "create_interface",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What skill are you having issues with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Entity Recognition",
                    "text": "Entity Recognition"
                },
                {
                    "value": "Key Phrase Extraction",
                    "text": "Key Phrase Extraction"
                },
                {
                    "value": "Language Detection",
                    "text": "Language Detection"
                },
                {
                    "value": "Text Translation",
                    "text": "Text Translation"
                },
                {
                    "value": "Sentiment",
                    "text": "Sentiment"
                },
                {
                    "value": "Image Analysis",
                    "text": "Image Analysis"
                },
                {
                    "value": "OCR",
                    "text": "OCR"
                },
                {
                    "value": "Custom Entity Lookup",
                    "text": "Custom Entity Lookup"
                },
                {
                    "value": "Text Merge",
                    "text": "Text Merge"
                },
                {
                    "value": "Text Split",
                    "text": "Text Split"
                },
                {
                    "value": "Conditional",
                    "text": "Conditional"
                },
                {
                    "value": "Shaper",
                    "text": "Shaper"
                },
                {
                    "value": "Document Extraction",
                    "text": "Document Extraction"
                },
                {
                    "value": "Custom Web API",
                    "text": "Custom Web API"
                },
                {
                    "value": "Custom AML (preview)",
                    "text": "Custom AML (preview)"
                },
                {
                    "value": "PII Detection (preview)",
                    "text": "PII Detection (preview)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---