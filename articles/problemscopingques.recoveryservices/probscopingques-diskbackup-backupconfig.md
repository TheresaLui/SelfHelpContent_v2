<properties
         pageTitle="Scoping questions for Azure Disk Backup configuration failure"
         description="Scoping questions for Azure Disk Backup configuration failure"
         authors="kapilgoyal"
         ms.author="kagoya"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32785497,32785498,32785499"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="f54e681f-a2e3-41d9-b60e-7a342efb61ea"
         ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure Disk Backup configuration failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Disk Backup configuration failure",
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
                    "value": "Snapshot Data store Resource Group parameter is not provided or is invalid.",
                    "text": "Snapshot Data store Resource Group parameter is not provided or is invalid."
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
