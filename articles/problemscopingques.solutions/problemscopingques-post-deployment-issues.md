<properties
	articleId="problemscopingques-post-deployment-issues.md"
	pageTitle="Service Catalog - Post-deployment Issues"
	description="Service Catalog - Post-deployment Issues"
	authors="apclouds"
	ms.author="angperez"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628298,32628300,32628301,32628295,32628294"
	productPesIds="16651"
	cloudEnvironments="public, fairfax, usnat, ussec, mooncake"
	schemaVersion="1"
	ownershipId="Compute_AzureManagedApplications"
/>
# Managed Application Post-deployment Issues
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Creating Managed Application Definitions",
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
            "id": "managed_application_id",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide your managed application ID",
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
            "id": "deployment_tool",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "Please provide what tool was used to deploy the managed application (PowerShell, Azure CLI, Portal, REST API)",
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
