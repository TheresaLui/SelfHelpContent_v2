<properties
	articleId="ac26fa9c-05b3-467a-b5e4-49812c98d489"
	pageTitle="Scoping Questions for PoweShell and SDK Experience"
	description="Scoping Questions for PoweShell and SDK Experience"
	authors="TobyTu"
	ms.author="mquian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742537"
	productPesIds="15791"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# PoweShell and SDK Experience
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "PoweShell and SDK Experience",
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
            "id": "cmd_sdk",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the failed PowerShell command or SDK method.",
            "watermarkText": "Enter the command or SDK method",
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
