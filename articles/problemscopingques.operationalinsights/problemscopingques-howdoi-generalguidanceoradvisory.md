
<properties
pageTitle="General Guidance or Advisory"
description="General Guidance or Advisory"
articleId="problemscopingques-General_Guidance_or_Advisory"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32613150"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# General Guidance or Advisory
---
{
    "resourceRequired": true,
    "title": "General Guidance or Advisory",
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
            "id": "single_multiple_machines",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is your desired goal by contacting Microsoft Support today?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I Can’t find the information in product documentation",
                    "text": "I Can’t find the information in product documentation"
                },
                {
                    "value": "I have an issue but can’t find a suitable support topic for it",
                    "text": "I have an issue but can’t find a suitable support topic for it"
                },
                {
                    "value": "General question",
                    "text": "General question"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---