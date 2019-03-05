
<properties
pageTitle="Restore deleted workspace"
description="Restore deleted workspace"
articleId="problemscopingques-Restore_deleted_workspace"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612520"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
/>

# Restore deleted workspace
---
{
    "resourceRequired": true,
    "title": "Restore deleted workspace",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "recovery_support_information",
            "order": 1,
            "controlType": "infoblock",
            "content": "Workspace recovery is possible up to 14 days after the deletion. The deleted workspace is permanently purged and unrecoverable after 14 days"
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When was the workspace deleted?",
            "required": true
        },
        {
            "id": "workspace_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the workspace name to recover?",
            "watermarkText": "Enter the workspace name",
            "required": false
        },
        {
            "id": "workspace_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the workspace ID to recover?",
            "watermarkText": "e.g. 12345678-dd3c-4e38-b4db-38dc57fdee7b",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---