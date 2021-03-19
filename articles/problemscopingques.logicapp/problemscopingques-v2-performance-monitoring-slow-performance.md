<properties
    articleId="mc42cf9c-05b3-437a-a5e4-49812c08d489"
    pageTitle="Scoping Questions for Slow Performance"
    description="Scoping Questions for Slow Performance"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32780518"
    productPesIds="17378"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_LogicApps"
/>
# Slow Performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Slow Performance",
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
            "id": "run_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide run ID(s) that are experiencing the issue.",
            "watermarkText": "Enter the ID(s)",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
