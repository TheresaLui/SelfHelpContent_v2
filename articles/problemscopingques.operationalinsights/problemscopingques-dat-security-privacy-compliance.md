
<properties
pageTitle="Data security, privacy and compliance"
description="Data security, privacy and compliance"
articleId="problemscopingques-dat-security-privacy-compliance"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32690787"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Data security, privacy and compliance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Data security, privacy and compliance",
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
            "id": "issue",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the issue related with a potential data breach or security issue?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
           {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Please provide any additional information in regards to your issue",
            "required": true,
            "hints": []
        }
    ]
}
---
