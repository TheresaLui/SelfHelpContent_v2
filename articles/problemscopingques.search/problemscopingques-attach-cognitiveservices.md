<properties
	pageTitle="Issue attaching a cognitive service resource"
	description="Issue attaching a cognitive service resource"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681353"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="8155a9b8-8a17-4a05-9d04-15bdb8380f85"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue attaching a cognitive service resource
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue attaching a cognitive service resource",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "cognitive_service",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you using a free or paid cognitive service subscription?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Free",
                    "text": "Free"
                },
                {
                    "value": "Paid",
                    "text": "Paid"
                }
            ],
            "required": false
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
