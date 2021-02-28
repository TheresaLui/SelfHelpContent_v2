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
    "fileAttachmentHint": "If possible, please attach a file containing the JSON definition of the skillset you are trying to create.",
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
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to create this skillset?",
            "required": true
        },
        {
            "id": "create_interface",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How are you creating the skillset?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "REST",
                    "text": "Programmatically, using REST APIs"
                },
                {
                    "value": "SDK",
                    "text": "Programmatically, using SDK"
                },
                {
                    "value": "Portal_Import_Data",
                    "text": "Using the Azure Portal - Import Data Flow"
                },
                {
                    "value": "Portal_New_Skillset",
                    "text": "Using the Azure Portal - New Skillset"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---