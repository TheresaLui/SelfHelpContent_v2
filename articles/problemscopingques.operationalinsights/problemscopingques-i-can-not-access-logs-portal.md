
<properties
pageTitle="I cannot access Logs portal"
description="I cannot access Logs portal"
articleId="problemscopingques-i-can-not-access-logs-portal"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32727886"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# I cannot access 'Logs' portal
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "I cannot access 'Logs' portal",
    "fileAttachmentHint": "If possible, please upload screenshots and additional attachments which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "prevously_worked",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Has this previously worked?",
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
            "id": "browser_occurrence",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Is the issue occurring on all browsers?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "All browsers",
                    "text": "All browsers"
                },
                {
                    "value": "Just one browser",
                    "text": "Just one browser"
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
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where applicable. If this only happening on a specific browser, please specify the browser name and version.",
            "required": true,
            "hints": []
        }
    ]
}
---
