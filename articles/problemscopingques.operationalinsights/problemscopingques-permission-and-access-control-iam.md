
<properties
pageTitle="Permissions and access control (IAM)"
description="Permissions and access control (IAM)"
articleId="problemscopingques-permission-and-access-control-iam"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612439"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Permissions and access control (IAM)
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Permissions and access control (IAM)",
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
            "id": "users",
            "order": 4,
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
            "id": "itermittent_or_consistant",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the issue intermittent or constant?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Itermittent",
                    "text": "Itermittent"
                },
                {
                    "value": "Consistant",
                    "text": "Consistant"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "consistant",
            "order": 8,
            "visibility": "itermittent_or_consistant == Consistant",
            "controlType": "multilinetextbox",
            "displayLabel": "As the issue is constant, would you please describe how to reproduce the issue?",
            "watermarkText": "Please write the detailed steps to reproduce the issue",
            "required": true
        },
                {
            "id": "lighthouse",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Do you have Azure Lighthouse in your environment?",
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
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of any error messages where available. Please also enumerate the Azure resource(s) where you're facing the issue.",
            "required": true,
            "hints": []
        }
    ]
}
---
