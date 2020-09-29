<properties
                pageTitle="Virtual Disk Management"
                description="Virtual Disk Management"
                authors="timbasham"
                ms.author="tibasham"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32730257"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="3db8d405-735d-44a3-891a-1bdab3651f62"
                ownershipId="Compute_VirtualMachines_Content"
/>
# Virtual Disk Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Linux Guest OS Disk Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "virtualdisk_createdelete",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this a new or existing VHD?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "New",
                    "text": "New"
                },
                {
                    "value": "Existing",
                    "text": "Existing"
                }
            ],
            "required": false
        },
        {
            "id": "virtualdisk_task",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the task you are trying to perform?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create or expand an LVM volume",
                    "text": "Create or expand an LVM volume"
                },
                {
                    "value": "Create or expand an mdadm volume",
                    "text": "Create or expand an mdadm volume"
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
