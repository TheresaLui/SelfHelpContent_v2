<properties
	articleId="problemscopingques-hybridworker.md"
	pageTitle="Azure Automation - Hybrid Worker"
	description="Azure Automation - Hybrid Worker"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599857,32599920,32599939"
	productPesIds="15607"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_Automation"
/>
# Hybrid Worker
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Hybrid Worker",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "NodeName",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the computer name of the hybrid worker",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Paste in the exact text of any errors that occurred."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
