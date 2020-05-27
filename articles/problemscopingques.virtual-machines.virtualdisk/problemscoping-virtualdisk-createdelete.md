<properties
                pageTitle="Virtual Disk Management"
                description="Virtual Disk Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32632140"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0073"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Virtual Disk Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Creating or deleting virtual disks",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "virtualdisk_createdelete",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to create or delete a virtual disk?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create",
                    "text": "Create"
                },
                {
                    "value": "Delete",
                    "text": "Delete"
                }
            ],
            "required": false
        },
        {
            "id": "virtualdisk_task",
            "order": 2,
            "visibility": "virtualdisk_createdelete == Create",
            "controlType": "dropdown",
            "displayLabel": "What is the task you are trying to perform?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create or expand a storage pool configuration",
                    "text": "Create or expand a storage pool configuration"
                },
                {
                    "value": "Expand a Windows volume",
                    "text": "Expand a Windows volume"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
