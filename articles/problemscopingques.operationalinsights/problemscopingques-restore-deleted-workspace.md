
<properties
pageTitle="Restore deleted workspace"
description="Restore deleted workspace"
articleId="problemscopingques-restore-deleted-workspace"
authors="neilghuman"
ms.author="neghuman"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612520"
productPesIds="15725"
cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
schemaVersion="1"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Restore deleted workspace
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Restore deleted workspace",
    "fileAttachmentHint": "If possible, please upload screenshots and any additional attachments which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "workspace",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the workspace name or workspace ID of the deleted workspace?",
            "watermarkText": "Enter the 32 characters workspace ID or the workspace name",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "how_method",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Which method was utilized to delete the workspace?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Soft-delete",
                    "text": "Soft-delete"
                },
                {
                    "value": "Permanent-delete",
                    "text": "Permanent-delete"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know / Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Please provide any additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---
