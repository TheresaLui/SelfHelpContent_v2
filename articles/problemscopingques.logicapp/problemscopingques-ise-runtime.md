<properties
    articleId="ac26fa9c-05b3-487a-b5e4-49815c98d489"
    pageTitle="Scoping Questions for Runtime"
    description="Scoping Questions for Runtime"
    authors="TobyTu"
    ms.author="mquian"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32742541"
    productPesIds="15791"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="Compute_LogicApps"
/>
# Runtime
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Runtime",
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
            "id": "error_message",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the full error message.",
            "watermarkText": "Enter the error message",
            "required": false
        },
        {
            "id": "ise_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the ISE name.",
            "watermarkText": "Enter the ISE name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the problem.",
            "watermarkText": "Please provide the detailed symptom and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
