<properties
	articleId="problemscopingques-portal-tags.md"
	pageTitle="Issue with tags"
	description="Issue with tags"
	authors="rthorn17"
	ms.author="rithorn"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637530"
	productPesIds="15739"
	cloudEnvironments="public, Fairfax, usnat, ussec, blackforest, mooncake"
	schemaVersion="1"
	ownershipId="Compute_AzurePortal"
/>

# Tag Issues
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Tag Issue",
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
            "id": "problem_scope",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Select the scope where you are having tag issues with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                  "value": "Resource",
                  "text": "Resource"
                },
                {
                  "value": "Resource Group",
                  "text": "Resource Group"
                },
                {
                  "value": "Subscription",
                  "text": "Subscription"
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