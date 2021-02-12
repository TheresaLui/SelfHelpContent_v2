<properties
	articleId="problemscopingques-management-issues.md"
	pageTitle="Azure Management Groups - Management Groups"
	description="Azure Management Groups - Management Groups"
	authors="apclouds"
	ms.author="angperez"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743300,32743301,32743302,32743303,32743304,32743299"
	productPesIds="16530"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ARM_ManagementGroups"
/>
# Management Groups
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Management Groups",
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
            "id": "management_group_id",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide your management group ID",
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
            "id": "client_tools",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Select the client tool being used",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                  "value": "Azure Portal",
                  "text": "Azure Portal"
                },
                {
                  "value": "Azure CLI",
                  "text": "Azure CLI"
                },
                {
                  "value": "PowerShell",
                  "text": "PowerShell"
                },
                {
                  "value": "REST API",
                  "text": "REST API"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
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
