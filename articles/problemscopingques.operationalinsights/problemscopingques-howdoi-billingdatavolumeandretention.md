
<properties
pageTitle="Billing data volume and retention"
description="Billing data volume and retention"
articleId="problemscopingques-billing_data_volume_and_retention"
authors="yossiy, neilghuman"
ms.author="yossiy, neghuman"
selfHelpType="problemScopingQuestions"
displayOrder=""
supportTopicIds="32612512"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Billing data volume and retention
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Restore deleted workspace",
    "fileAttachmentHint": "Please provide a screenshot including any dashboard or view of where you're seeing the billing and/or usage issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "disputing_charge",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you disputing a charge on your bill?",
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
                    "text": "Not sure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is your current data retention setting in days?",
            "watermarkText": "e.g. 31, 90, 180, etc.",
            "required": false
        },
        {
            "id": "usage_query",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": false,
            "displayLabel": "If the issue is usage related, kindly provide query used to retrieve data set.",
            "watermarkText": "Please enter the full query being executed, including the time interval",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible including what changes might have happened in the environment that might be related with the issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---