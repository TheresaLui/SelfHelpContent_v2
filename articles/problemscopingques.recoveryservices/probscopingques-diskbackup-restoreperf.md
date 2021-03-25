<properties
         pageTitle="Scoping questions for Azure Disk Backup restore performance"
         description="Scoping questions for Azure Disk Backup restore performance"
         authors="kapilgoyal"
         ms.author="kagoya"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32785504"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="6a79fe6f-d53c-491c-8a4e-61c6ace10c07"
         ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure Disk Backup restore performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Disk Backup restore performance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "disk_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide details for the disk that is experiencing the problem",
            "watermarkText": "Enter the disk-name that is experiencing the problem",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup job Activity ID",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b ",
            "required": false
        },
        {
            "id": "backup_completed",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Has the backup ever completed successfully?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "backup_job_starttime",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "How long has the job been running?",
            "required": false
        },
        {
            "id": "select_ErrorMessage",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Select the error message you are seeing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Permission issues on the Target Resource Group",
                    "text": "Permission issues on the Target Resource Group"
                },
                {
                    "value": "Restore failed as a Disk with same name already exists in the selected Target Resource Group",
                    "text": "Restore failed as a Disk with same name already exists in the selected Target Resource Group"
                },
                {
                    "value": "Target Resource Group does not exist.",
                    "text": "Target Resource Group does not exist."
                },
                {
                    "value": "The disk snapshot(metadata) for this Restore point has been deleted.",
                    "text": "The disk snapshot(metadata) for this Restore point has been deleted."
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
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
