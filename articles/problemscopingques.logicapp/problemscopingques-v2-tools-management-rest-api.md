<properties
	articleId="ac26fa9c-05b3-9001-b5e4-49812c98d489"
	pageTitle="Scoping Questions for REST API"
	description="Scoping Questions for REST API"
	authors="genlin"
	ms.author="kawilson"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32780509"
	productPesIds="17378"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# REST API
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "REST API",
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
            "id": "api_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the failed API name",
            "watermarkText": "Enter the name",
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
