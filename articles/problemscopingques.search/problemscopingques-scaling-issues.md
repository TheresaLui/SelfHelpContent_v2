<properties
	pageTitle="Issue adding or removing partitions or replicas"
	description="Issue adding or removing partitions or replicas"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681352"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="7119e191-4d45-4151-b969-5b49429905e2"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue adding or removing partitions or replicas
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue adding or removing partitions or replicas",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the issue you experienced",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error text when possible."
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "arm_template",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What scaling operation would you like to perform?",
            "required": false,
            "watermarkText": "Example: Add 1 partition and 2 replicas"
        },
        {
            "id": "create_interface",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What client did you use?",
            "watermarkText": "Choose an option",
            "required": true,
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
                    "value": "ARM Template",
                    "text": "ARM Template"
                },
                {
                    "value": "Custom client using the Management API or SDK",
                    "text": "Custom client using the Management API or SDK"
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
