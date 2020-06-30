<properties
	articleId="problemscopingques-assignments.md"
	pageTitle="Azure Blueprint - Blueprint Assignments"
	description="Azure Blueprint - Blueprint Assignments"
	authors="apclouds"
	ms.author="angperez"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739603,32739604,32739606,32739608,32739601"
	productPesIds="16600"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AzureBlueprint"
/>
# Blueprint Assignments
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Blueprint Assignments",
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
            "id": "blueprint_assignment_id",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide your blueprint assignment ID",
            "required": false
        },
        {
            "id": "error_message",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the error message",
            "required": false
        },
        {
            "id": "assignment_tool",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Please provide what tool was used to assign the blueprint (PowerShell, Azure CLI, Portal, REST API)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 50,
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
