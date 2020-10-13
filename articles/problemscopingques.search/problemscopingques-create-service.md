<properties
	pageTitle="Issue creating a Search service"
	description="Issue creating a Search service"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681355"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="19ac41e7-7222-41c2-bb18-1542db3661d6"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue creating a Search service
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue creating a Search service",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "create_error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "create_interface",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What client did you use to create the service?",
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
            "id": "create_before",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": :"Did you previously have a search service by the same name?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to create the service?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
