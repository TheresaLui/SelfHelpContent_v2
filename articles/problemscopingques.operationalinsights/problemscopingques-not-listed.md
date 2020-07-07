
<properties
pageTitle="Not listed"
description="Not listed"
articleId="problemscopingques-not-listed"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612510"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Not listed
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Not listed",
    "fileAttachmentHint": "If possible, please upload screenshots and any additional attachments which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "type_of_issue",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue related with a solution or with Azure platform logs?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Solution",
                    "text": "Solution"
                },
                {
                    "value": "Platform",
                    "text": "Platform"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "solution",
            "order": 8,
            "visibility": "type_of_issue == Solution",
            "controlType": "textbox",
            "displayLabel": "What is the solution name?",
            "watermarkText": "Please enter the solution name as displayed on the Azure portal",
            "required": false
        },
        {
            "id": "platform",
            "order": 9,
            "visibility": "type_of_issue == Platform",
            "controlType": "textbox",
            "displayLabel": "What is the Azure platform log type and/or name?",
            "watermarkText": "Please enter the log type or name as displayed on the Azure portal",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available. Please also include any query details if applicable.",
            "required": true,
            "hints": []
        }
    ]
}
---
