<properties
	articleId="ac26fa9c-05b3-487a-b5e4-49814c98d489"
	pageTitle="Scoping Questions for Network Health"
	description="Scoping Questions for Network Health"
	authors="TobyTu"
	ms.author="mquian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742533"
	productPesIds="15791"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# Network Health
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Network Health",
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
            "id": "ise_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the ISE name.",
            "watermarkText": "Enter the ISE name",
            "required": false
        },
        {
            "id": "network_detail",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide network health details from the Azure portal.",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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
Please provide Network Health Details from the Azure portal