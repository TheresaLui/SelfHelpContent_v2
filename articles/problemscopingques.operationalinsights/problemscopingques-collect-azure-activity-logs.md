
<properties
pageTitle="Collect Azure Activity logs"
description="Collect Azure Activity logs"
articleId="problemscopingques-collect-azure-activity-logs"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612422"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Collect Azure Activity logs
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Collect Azure Activity logs",
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
            "id": "workspace_location",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the Log Analytics workspace located on the same subscription where you've configured the data to be collected?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Same subscription",
                    "text": "Same subscription"
                },
                {
                    "value": "Different subscription on the same tenant",
                    "text": "Different subscription on the same tenant"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "activity_data",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is all the Azure Activity data missing, incomplete or incorrect?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Activity data is missing",
                    "text": "Azure Activity data is missing"
                },
                {
                    "value": "Azure Activity data is showing up, but some details are incomplete",
                    "text": "Azure Activity data is showing up, but some details are incomplete"
                },
                {
                    "value": "Azure Activity data is showing up, but some details are incorrect",
                    "text": "Azure Activity data is showing up, but some details are incorrect"
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
            "order": 9,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available.",
            "required": true,
            "hints": []
        }
    ]
}
---
