
<properties
pageTitle="ARM templates, PowerShell and CLI"
description="ARM templates, PowerShell and CLI"
articleId="problemscopingques-ARM_templates_PowerShell_and_CLI"
authors="yossiy,neilghuman"
ms.author="yossiy,neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612544"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# ARM templates, PowerShell and CLI
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Restore deleted workspace",
    "fileAttachmentHint": "Please provide a screenshot of any errors and please also attach all relevant JSON files related with the ARM template. JSON files must be compressed and uploaded in ZIP format.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "users",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue happening to a single user or multiple users?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Single user",
                    "text": "Single user"
                },
                {
                    "value": "Multiple users",
                    "text": "Multiple users"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What method are you using to deploy the template?",
            "watermarkText": "e.g. PowerShell, CLI, etc.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available. Provide the commands being executed (PowerShell or Azure CLI).",
            "required": true,
            "hints": [
                {
                    "text": "Please include the exact text of any error message"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---