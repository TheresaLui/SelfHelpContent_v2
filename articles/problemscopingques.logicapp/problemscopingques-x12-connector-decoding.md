<properties
	articleId="ac91ca9c-05b3-437a-a5e4-49812c98d489"
	pageTitle="Scoping Questions for X12 Decoding"
	description="Scoping Questions for X12 Decoding"
	authors="TobyTu"
	ms.author="mquian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742559"
	productPesIds="15791"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# X12 Decoding
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "X12 Decoding",
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
            "id": "run_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide one or more failed run ID(s).",
            "watermarkText": "Enter the ID(s)",
            "required": false
        },
        {
            "id": "raw_inputs",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide Raw Inputs of the failed action or trigger.",
            "watermarkText": "Enter the Raw Inputs",
            "required": false
        },
        {
            "id": "raw_outputs",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide Raw Outputs of the failed action or trigger.",
            "watermarkText": "Enter the Raw Outputs",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
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
