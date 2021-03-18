<properties
    articleId="ac26fa9c-05b3-487a-b5e4-12813c98d401"
    pageTitle="Scoping Questions for Deploying and Provisioning"
    description="Scoping Questions for Deploying and Provisioning"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32780463"
    productPesIds="17030"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    schemaVersion="1"
    ownershipId="Compute_LogicApps"
/>
# Deploying and Provisioning
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Deploying and Provisioning",
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
        },
        {
            "id": "ise_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the ISE name.",
            "watermarkText": "Enter the ISE name",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
