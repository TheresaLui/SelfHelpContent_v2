<properties
	pageTitle="Issue creating or updating a skillset"
	description="Issue creating or updating a skillset"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681358"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="3f0a94f2-c7fb-48a0-979d-d156e4e10755"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue creating or updating a skillset
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue creating or updating a skillset",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the issue you experienced",
            "useAsAdditionalDetails": true,
            "required": true,
	    "watermarkText":"Please provide the full error text when possible."
        },
        {
            "id": "service_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name of the search service you tried to create?",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to create the search service?",
            "required": true
        },
        {
            "id": "previously_exist",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you recently deleted a search service with the same name?",
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
            "id": "create_interface",
            "order": 5,
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
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---