<properties
	pageTitle="Issue using the Azure CLI or Powershell"
	description="Issue using the Azure CLI or Powershell"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681373"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="9b6f4cd2-551c-46d8-9e8a-e216cd6019a0"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue using the Azure CLI or Powershell
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue using the Azure CLI or Powershell",
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
            "id": "problem_cli_ps",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you using the Azure CLI or PowerShell?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "PowerShell",
                    "text": "PowerShell"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ]
        },
        {
            "id": "problem_version",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What version of Azure CLI or PowerShell are you using?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
