<properties
    articleId="mc43cf9c-05b3-437a-a5e4-49812c08d489"
    pageTitle="Scoping Questions for Alerts and Functions"
    description="Scoping Questions for Alerts and Functions"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32780474"
    productPesIds="17378"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_LogicApps"
/>
# Alerts and Functions
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Alerts and Functions",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the problem.",
            "watermarkText": "Please provide the detailed symptom and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the full error message.",
            "watermarkText": "Enter the error message",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
