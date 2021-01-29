
<properties
pageTitle="Link or unlink automation account"
description="Link or unlink automation account"
articleId="problemscopingques-Link_or_unlink_automation_account"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612473"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Link or unlink automation account
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Link or unlink automation account",
    "fileAttachmentHint": "Provide a screenshot of the error",
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
            "displayLabel": "What error are you seeing?",
            "watermarkText": "Please enter the error message",
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