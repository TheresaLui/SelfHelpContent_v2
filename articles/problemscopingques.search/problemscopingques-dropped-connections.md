<properties
	pageTitle="Dropped or terminated connections"
	description="Dropped or terminated connections"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681346"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="d18a75f8-45bf-4b70-8703-b4b7ea9e4b5f"
	ownershipId="AzureSearch_AzureSearch"
/>
# Dropped or terminated connections
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Dropped or terminated connections",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the connectivity issue you experienced",
            "useAsAdditionalDetails": true,
            "required": true,
	    "watermarkText":"Please provide the full error text when possible."
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last experience a connectivity issue?",
            "required": true
        },
        {
            "id": "client_used",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What client were you using to connect?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Search Explorer in Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "Custom client using the REST API",
                    "text": "Custom client using REST API"
                },
                {
                    "value": "Custom client using an SDK",
                    "text": "Custom client using an SDK"
                },
                {
                    "value": "Postman",
                    "text": "Postman"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "ip_firewall",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Do you have an IP firewall enabled on the search service?",
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
            "id": "private_mode",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is your search service endoint public or private?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Public",
                    "text": "Public"
                },
                {
                    "value": "Private",
                    "text": "Private"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
