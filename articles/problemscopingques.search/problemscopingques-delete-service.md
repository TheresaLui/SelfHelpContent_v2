<properties
	pageTitle="Issue deleting a Search service"
	description="Issue deleting a Search service"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681361"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="8cbb489b-6508-48a5-9b49-0b3089f38ea0"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue deleting a Search service
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue deleting a Search service",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "delete_error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "delete_interface",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What client did you use to delete the service?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "Powershell",
                    "text": "Powershell"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "Custom client using Management API or SDK",
                    "text": "Custom client using Management API or SDK"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to delete the service?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
