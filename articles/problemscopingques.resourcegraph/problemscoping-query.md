<properties
	articleId="problemscopingques-query.md"
	pageTitle="Azure Resource Graph - Resource Graph Query"
	description="Azure Resource Graph - Resource Graph Query"
	authors="apclouds"
	ms.author="angperez"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636056"
	productPesIds="16716"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="compute_azureresourcegraph"
/>
# Resource Graph Query
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Resource Graph Query",
    "fileAttachmentHint": "Please provide a query file and screenshot of any errors",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "resource_graph_query",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide your resource graph query",
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
            "id": "expected_behavior",
            "order": 40,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the expected behavior?",
            "required": false
        },
        {
            "id": "current_behavior",
            "order": 50,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the current behavior?",
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
