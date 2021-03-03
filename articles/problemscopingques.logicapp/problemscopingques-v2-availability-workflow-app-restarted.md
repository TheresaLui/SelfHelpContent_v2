<properties
	articleId="ac26fa9c-05b3-4010-b5e4-49812c98d489"
	pageTitle="Scoping Questions for Workflow App Restarted"
	description="Scoping Questions for Workflow App Restarted"
	authors="genlin"
	ms.author="kawilson"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32780527"
	productPesIds="17378"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# Workflow App Restarted
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Workflow App Restarted",
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
            "id": "problem_description",
            "order": 3,
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
