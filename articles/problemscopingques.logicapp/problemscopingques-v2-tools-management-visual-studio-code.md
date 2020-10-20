<properties
	articleId="ac26fa9c-05b3-0003-b5e4-49812c98d489"
	pageTitle="Scoping Questions for Visual Studio"
	description="Scoping Questions for Logic Apps with Visual Studio Code"
	authors="genlin"
	ms.author="kawilson"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32780524"
	productPesIds="17378"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# Logic Apps with Visual Studio Code
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Visual Studio Code",
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
            "displayLabel": "Please copy and paste the Logic Apps log from Output Windows into the following box",
            "watermarkText": "Enter the Logic Apps log",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---