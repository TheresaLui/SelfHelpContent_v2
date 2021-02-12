<properties
pageTitle="ARM and PowerShell Issues"
description="ARM and PowerShell Issues"
service="microsoft.eventgrid"
resource="arm-ps-issues"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32583165"
resourceTags=""
productPesIds="16263"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eg-arm-ps-issues"
schemaVersion="1"
	ownershipId="AzureEventGrid_Topics"
/>
# ARM and PowerShell Issues
---
{
    "subscriptionRequired": true,
    "title": "ARM and PowerShell Issues",
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
         {
            "id": "problem_cli_ps",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you using CLI or PowerShell?",
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
                    "value": "DontKnow",
                    "text": "I don't know"
                }
            ]
        },
         {
            "id": "problem_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What version of CLI or PowerShell are you using",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
           "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description details"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---