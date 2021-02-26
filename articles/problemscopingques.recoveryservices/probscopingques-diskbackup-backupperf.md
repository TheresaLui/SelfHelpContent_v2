<properties
         pageTitle="Scoping questions for Azure Disk Backup performance"
         description="Scoping questions for Azure Disk Backup performance"
         authors="kapilgoyal"
         ms.author="kagoya"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32785496"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="5c3a9da3-264b-4015-82c5-2f0eda088615"
         ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure Disk Backup performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Disk Backup performance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "disk_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide details for the disk that is experiencing the problem",
            "watermarkText": "Enter the disk-name that you are trying backup",
            "required": true
        },
        {
            "id": "select_ErrorMessage",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Has the backup ever successfully completed?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "YES",
                    "text": "YES"
                },
                {
                    "value": "NO",
                    "text": "NO"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
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
