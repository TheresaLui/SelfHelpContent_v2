<properties
    articleId="ac26fa9c-05b3-487a-b5e4-12813c98d404"
    pageTitle="Scoping Questions for TLS SSL Error"
    description="Scoping Questions for TLS SSL Error"
    authors="TobyTu"
    ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32780467"
    productPesIds="17030"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    schemaVersion="1"
    ownershipId="Compute_LogicApps"
/>
# TLS SSL Error
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "TLS SSL Error",
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
        },
        {
            "id": "run_id",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide one or more failed run ID(s).",
            "watermarkText": "Enter the ID(s)",
            "required": false
        },
        {
            "id": "raw_inputs",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide Raw Inputs of the failed action or trigger.",
            "watermarkText": "Enter the Raw Inputs",
            "required": false
        },
        {
            "id": "raw_outputs",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide Raw Outputs of the failed action or trigger.",
            "watermarkText": "Enter the Raw Outputs",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
