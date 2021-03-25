<properties
	pageTitle="Custom recommendations"
	description="Custom recommendations"
	authors="genlin"
	ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32787447"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="b1b6273d-908e-4f2d-9112-36a830ea0107"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Custom recommendations in security center
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Custom recommendations in security center",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "resource_type",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Enter the resource ID that you want to investigate the billing problem",
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
