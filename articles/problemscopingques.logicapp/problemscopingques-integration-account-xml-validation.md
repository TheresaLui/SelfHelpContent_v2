<properties
	articleId="ac80ca9c-15b3-437a-a5e4-49812c98d489"
	pageTitle="Scoping Questions for XML Validation"
	description="Scoping Questions for XML Validation"
	authors="TobyTu"
	ms.author="mquian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742562"
	productPesIds="15791"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# XML Validation
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "XML Validation",
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
            "id": "xslt_map",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide XSLT map.",
            "watermarkText": "Enter the XSLT map",
            "required": false
        },
        {
            "id": "sample_message",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide a sample message to be transformed by the XSLT map.",
            "watermarkText": "",
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
