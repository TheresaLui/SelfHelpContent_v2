<properties
	articleId="problemscopingques-portal-template.md"
	pageTitle="Issue with ARM Template"
	description="Issue with ARM Template"
	authors="rthorn17"
	ms.author="rithorn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637529"
	productPesIds="15739"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AzurePortal"
/>

# ARM Template Deployment Issue
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "ARM Template Deployment Issue",
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
            "id": "problem_correlation-id",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "If you have the Correlation ID, please provide it",
            "required": false
        },
        {
            "id": "problem_scope",
            "order": 30,
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
            "id": "problem_description",
            "order": 40,
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