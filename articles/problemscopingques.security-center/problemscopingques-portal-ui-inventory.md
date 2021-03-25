<properties
	pageTitle="Portal and UI/Inventory in security center"
	description="Portal and UI/Inventory in security center"
	authors="genlin"
	ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32788565"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="b1b6273d-908e-4f2d-2011-36a830ea0107"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Portal and UI/Inventory in security center
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Portal and UI/Inventory in security center",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "resource_type",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Enter the resource type that you have problem with",
            "watermarkText": "Example: Virtual Machine",
            "required": true
        },
      {
                    "id": "issue_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Select the issue you're requesting support for",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Resource is missing",
                            "text": "Resource is missing"
                        },
                        {
                            "value": "Resource details mismatch",
                            "text": "Resource details mismatch"
                        },
                        {
                            "value": "CSV Report Issue",
                            "text": "CSV Report Issue"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other"
                        }
                    ],
                    "required": true
                },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
