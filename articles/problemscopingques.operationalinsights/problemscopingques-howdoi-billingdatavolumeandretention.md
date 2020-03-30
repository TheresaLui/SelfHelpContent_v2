
<properties
pageTitle="Billing, data volume and retention"
description="Billing, data volume and retention"
articleId="problemscopingques-Billing_data_volume_and_retention"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612512"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Billing, data volume and retention
---
{
    "resourceRequired": true,
    "title": "Restore deleted workspace",
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
            "id": "is_it_azure_vm",
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