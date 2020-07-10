
<properties
pageTitle="Azure Resource Manager (ARM) templates"
description="Azure Resource Manager (ARM) templates"
articleId="problemscopingques-Azure_Resource_Manager_ARM_templates"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612430"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Azure Resource Manager (ARM) templates
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Resource Manager (ARM) templates",
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
            "id": "alert_rule",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which alert rule has this problem?",
            "watermarkText": "Enter alert rule name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Error messages"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---