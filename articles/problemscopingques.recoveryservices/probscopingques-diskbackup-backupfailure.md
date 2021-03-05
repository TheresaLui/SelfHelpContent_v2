<properties
         pageTitle="Scoping questions for Azure Disk Backup failure"
         description="Scoping questions for Azure Disk Backup failure"
         authors="kapilgoyal"
         ms.author="kagoya"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32785495,32785494"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="7524bd38-e9e4-4b1b-9503-756144e5fb5b"
         ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure Disk Backup failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Disk Backup failure",
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
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b ",
            "required": false
        },
        {
            "id": "select_ErrorMessage",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the error message that you are seeing",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Invalid subscription selected for Snapshot Data store",
                    "text": "Invalid subscription selected for Snapshot Data store"
                },
                {
                    "value": "Unsupported disk type",
                    "text": "Unsupported disk type"
                },
                {
                    "value": "Snapshot Data store Resource Group do not exist",
                    "text": "Snapshot Data store Resource Group do not exist"
                },
                {
                    "value": "Managed Disk no longer exists",
                    "text": "Managed Disk no longer exists"
                },
                {
                    "value": "Permission issues on the Disk (or) Snapshot Data store Resource Group",
                    "text": "Permission issues on the Disk (or) Snapshot Data store Resource Group"
                },
                {
                    "value": "Disk quota maximum limit has been reached on the subscription.",
                    "text": "Disk quota maximum limit has been reached on the subscription."
                },
                {
                    "value": "Maximum number of allowed concurrent operations has reached for this operation type",
                    "text": "Maximum number of allowed concurrent operations has reached for this operation type"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
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
    ],
    "$schema": "SelfHelpContent"
}
---
