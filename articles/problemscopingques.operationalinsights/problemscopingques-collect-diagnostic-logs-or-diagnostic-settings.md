
<properties
pageTitle="Collect Diagnostics logs or Diagnostics Settings"
description="Collect Diagnostics logs or Diagnostics Settings"
articleId="problemscopingques-collect-diagnostic-logs-or-diagnostic-settings"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32633017"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Collect Diagnostics logs or Diagnostics Settings
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Collect Diagnostics logs or Diagnostics Settings",
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
            "id": "prevously_worked",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the Azure Diagnostic data missing, incomplete or incorrect?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Diagnostic data is missing",
                    "text": "Azure Diagnostic data is missing"
                },
                {
                    "value": "Azure Diagnostic data is showing up, but some details are incomplete",
                    "text": "Azure Diagnostic data is showing up, but some details are incomplete"
                },
                                {
                    "value": "Azure Diagnostic data is showing up, but some details are incorrect",
                    "text": "Azure Diagnostic data is showing up, but some details are incorrect"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "resources",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the issue impacting only one Azure resource or multiple?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Only one Azure resource",
                    "text": "Only one Azure resource"
                },
                {
                    "value": "Multiple resource types",
                    "text": "Multiple resource types"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "legacy_or_resource",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you using legacy diagnostic settings or resource-specific?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Legacy diagnostic settings",
                    "text": "Legacy diagnostic settings"
                },
                {
                    "value": "Resource-specific settings",
                    "text": "Resource-specific settings"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "query_being_executed",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the query being executed?",
            "watermarkText": "Please enter the full query being executed, including the time interval",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available. Please include the resource URI of one or more of the impacted Azure resources.",
            "required": true,
            "hints": []
        }
    ]
}
---
