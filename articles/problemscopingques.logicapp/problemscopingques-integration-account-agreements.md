<properties
	articleId="ac82ca9c-05b3-437a-a5e4-49812c98d489"
	pageTitle="Scoping Questions for agreements"
	description="Scoping Questions for agreements"
	authors="TobyTu"
	ms.author="mquian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742493"
	productPesIds="15791"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# Agreements
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Agreements",
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
            "id": "json",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the partner JSON definition.",
            "watermarkText": "Enter the JSON definition",
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
