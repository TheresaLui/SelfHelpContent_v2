<properties
	articleId="problemscopingques-api-issues"
	pageTitle="Issues with programmatic interfaces"
	description="Issues with programmatic interfaces"
	authors="snehithm"
	ms.author="snmuvva"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629614, 32629615, 32629616, 32629617, 32629618, 32629619, 32629620"
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# Issues with programmatic interfaces
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issues with programmatic interfaces",
    "fileAttachmentHint": "Provide screenshots of request/response that has a problem",
    "formElements": [
        {
            "id": "cli_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which programmatic interface has this problem",
            "watermarkText": "Choose a programmatic interface",
            "dropdownOptions": [
                {
                    "value": "REST API",
                    "text": "REST API"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "PowerShell",
                    "text": "PowerShell"
                }
            ],
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
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Expected behavior, actual behavior"
                },
                {
                    "text": "Any troubleshooting done so far"
                },
                {
                    "text": "Timestamps"
                },
                {
                    "text": "Screenshots"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---