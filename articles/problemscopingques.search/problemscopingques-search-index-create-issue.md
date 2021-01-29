<properties
	pageTitle="Issue creating an index"
	description="Issue creating an index"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681356"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="5f48314c-1144-49de-bdf7-8220329cbc9d"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue creating an index
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue creating an index",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "create_error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received when you tried to create the index?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "index_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name of the index you tried to create?",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "delete_interface",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What client did you use to create the index?",
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
            "displayLabel": "When did you last attempt to delete the service?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---