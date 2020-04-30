<properties
	articleId="problemscopingques-change.md"
	pageTitle="Azure Automation - Change Tracking and Inventory"
	description="Azure Automation - Change Tracking and Inventory"
	authors="zjalexander"
	ms.author="zachal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599855,32599863,32599865, 32599918"
	productPesIds="15607"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_Automation"
/>
# Change Tracking
---
{
    "resourceRequired": true,
    "title": "Change Tracking and Inventory",
    "fileAttachmentHint": "Please provide a screenshot of any errors",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "NodeName",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide the computer name of one or more affected machines",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include the exact text of any error messages that occur"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
