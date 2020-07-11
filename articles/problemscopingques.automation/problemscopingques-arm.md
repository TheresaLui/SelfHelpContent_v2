<properties
	articleId="problemscopingques-arm.md"
	pageTitle="Azure Automation - Problems with ARM Template Deployments"
	description="Azure Automation - Problems with ARM Template Deployments"
	authors="apclouds"
	ms.author="angperez"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32641156,32641157,32641158"
	productPesIds="15607"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_ARM"
/>
# Problems with ARM Templates
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "ARM Deployment Errors",
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
            "id": "deployment_correlation_id",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide your Deployment Correlation ID",
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
            "id": "problem_scope",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Select the scope of the deployment",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                  "value": "Resource Group",
                  "text": "Resource Group"
                },
                {
                  "value": "Subscription",
                  "text": "Subscription"
                },
                {
                  "value": "Management Group",
                  "text": "Management Group"
                },
                {
                  "value": "Tenant",
                  "text": "Tenant"
                }
            ],
            "required": false
        },
        {
            "id": "deployment_tool",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "Please provide what tool was used to assign the blueprint (PowerShell, Azure CLI, Portal, REST API, Other)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 60,
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