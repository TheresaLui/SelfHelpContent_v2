<properties
	pageTitle="Issue creating a search service"
	description="Issue creating a search service"
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
# Issue creating a search service
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
            "displayLabel": "Describe the issue you experienced",
            "useAsAdditionalDetails": true,
            "required": false,
	    "watermarkText":"Please provide the full error text when possible."
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last receive an?",
            "required": true
        },
        {
            "id": "create_interface",
            "order": 3,
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
            "order": 4,
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
        }
    ],
    "$schema": "SelfHelpContent"
}
---
