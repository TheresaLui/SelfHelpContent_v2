<properties
	articleId="ac26fa9c-05b3-0099-b5e4-49812c98d489"
	pageTitle="Scoping Questions for Runs and Triggers History "
	description="Scoping Questions for Runs and Triggers History"
	authors="genlin"
	ms.author="kawilson"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32780510"
	productPesIds="17378"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# Runs and Triggers History
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Runs and Triggers History",
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
            "id": "ISE_ID",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the integration service environment (ISE) name.",
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