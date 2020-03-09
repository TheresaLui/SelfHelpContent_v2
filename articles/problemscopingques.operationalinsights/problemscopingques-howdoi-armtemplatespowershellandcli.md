
<properties
pageTitle="ARM templates, PowerShell and CLI"
description="ARM templates, PowerShell and CLI"
articleId="problemscopingques-ARM_templates_PowerShell_and_CLI"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612544"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# ARM templates, PowerShell and CLI
---
{
    "resourceRequired": true,
    "title": "Restore deleted workspace",
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
            "id": "attache_template",
            "order": 2,
            "controlType": "infoblock",
            "content": "Please attach the template below"
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What method are you using to deploy the template?",
            "watermarkText": "e.g. PowerShell, CLI, etc.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---