<properties
	pageTitle="Portal and UI/Empty blade or missing data page"
	description="Portal and UI/Empty blade or missing data page"
	authors="genlin"
	ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749428"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="b1b6273d-908e-4f2d-0221-36a830ea0107"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Portal and UI/Empty blade or missing data page
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Portal and UI/Empty blade or missing data page",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "RBAC_role",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What Azure RBAC roles are assigned with your account?",
            "watermarkText": "Example: Virtual Machine Contributor",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
