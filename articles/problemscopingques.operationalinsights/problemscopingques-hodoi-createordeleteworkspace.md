
<properties
pageTitle="Create or delete workspace"
description="Create or delete workspace"
articleId="problemscopingques-Create_or_delete_workspace"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612513"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Create or delete workspace
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Create or delete workspace",
    "fileAttachmentHint": "Provide a screenshot of the error in UI or CLI",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "interface",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which interface has this problem?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure portal",
                    "text": "Azure portal"
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
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What errors are you seeing?",
            "watermarkText": "Enter error message",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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