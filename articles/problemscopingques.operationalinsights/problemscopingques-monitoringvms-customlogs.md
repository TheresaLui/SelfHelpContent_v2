
<properties
pageTitle="Custom logs"
description="Custom logs"
articleId="problemscopingques-Custom_logs"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612533"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
/>

# Custom logs
---
{
    "resourceRequired": true,
    "title": "Custom logs",
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
            "id": "OS_source",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is this for Windows or Linux?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows",
                    "text": "Windows"
                },
                {
                    "value": "Linux",
                    "text": "Linux"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "custom_log_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the custom log name?",
            "watermarkText": "Enter the custom log name",
            "required": false
        },
        {
            "id": "learn_more_text",
            "order": 4,
            "controlType": "infoblock",
            "content": "Please attach an example of a log file"
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---