
<properties
pageTitle="How to query specific data"
description="How to query specific data"
articleId="problemscopingques-How_to_query_specific_data"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612464"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# How to query specific data
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "How to query specific data",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "inquiry_reason",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is this a guidance inquiry, or you are seeing a problem?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Guidance inquiry",
                    "text": "Guidance inquiry"
                },
                {
                    "value": "Problem",
                    "text": "Problem"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "interface",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which interface has this problem?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Logs portal",
                    "text": "Logs portal"
                },
                {
                    "value": "A solution",
                    "text": "A solution"
                },
                {
                    "value": "REST",
                    "text": "REST"
                },
                {
                    "value": "CLI",
                    "text": "CLI"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Describe the expected query result"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---