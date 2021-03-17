
<properties
pageTitle="Data appears with delay"
description="Data appears with delay"
articleId="problemscopingques-Non_VM_data_appears_with_delay"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32745411"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Data appears with delay
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Restore deleted workspace",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the workspace deleted?",
            "required": true
        },
        {
            "id": "latency_table",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "On what data type latency was observed?",
            "watermarkText": "E.g. SecurityEvent",
            "required": false
        },
        {
            "id": "latency_minutes",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the latency in minutes?",
            "watermarkText": "Enter the latency in minutes",
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