<properties
	articleId="ac26fa9c-05b3-0205-b5e4-49812c98d489"
	pageTitle="PowerShell and SDK Experience"
	description="Scoping Questions for PowerShell and SDK Experience."
	authors="genlin"
	ms.author="kawilson"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32780506"
	productPesIds="17378"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# PowerShell and SDK Experience
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "PowerShell and SDK Experience",
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
            "id": "cmd_sdk",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the failed PowerShell command or SDK method.",
            "watermarkText": "Enter the command or SDK method",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---