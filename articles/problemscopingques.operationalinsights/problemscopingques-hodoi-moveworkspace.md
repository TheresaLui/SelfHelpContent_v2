
<properties
pageTitle="Move workspace to a different subscription or resource group"
description="Move workspace to a different subscription or resource group"
articleId="problemscopingques-Move_workspace_to_a_different_subscription_or_resource_group"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612491"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Move workspace to a different subscription or resource group
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Move workspace to a different subscription or resource group",
    "fileAttachmentHint": "Provide a screenshot of the error in UI or CLI",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "interface",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which interface has this problem?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure portal",
                    "text": "Azure portal"
                },
                {
                    "value": "REST",
                    "text": "REST"
                },
                {
                    "value": "CLI",
                    "text": "CLI"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "installed_solutions",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are any of these solutions installed in the workspace?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Update Management",
                    "text": "Update Management"
                },
                {
                    "value": "Change Tracking",
                    "text": "Change Tracking"
                },
                {
                    "value": "Start/Stop VMs during off-hours",
                    "text": "Start/Stop VMs during off-hours"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What error are you seeing?",
            "watermarkText": "Enter the error message",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Describe if you have automation account linked to your workspace"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---