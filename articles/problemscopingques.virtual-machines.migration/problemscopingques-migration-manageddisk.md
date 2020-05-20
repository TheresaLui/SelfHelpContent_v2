<properties
                pageTitle="Migration and Move"
                description="Migration and Move"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32565835"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0104"
	ownershipId="Compute_VirtualMachines_Content"
/>
# VM Migration
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Managed disks migration",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "migration_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "migration_scenario",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which of the following scenarios applies to your migration?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Convert stand alone VMs and VMs in an availability set to managed disks",
                    "text": "Convert stand alone VMs and VMs in an availability set to managed disks"
                },
                {
                    "value": "A single VM from classic to Resource Manager on managed disks",
                    "text": "A single VM from classic to Resource Manager on managed disks"
                },
                {
                    "value": "All the VMs in a vNet from classic to Resource Manager on managed disks",
                    "text": "All the VMs in a vNet from classic to Resource Manager on managed disks"
                },
                {
                    "value": "All the VMs from one ResourceGroup to another ResourceGroup",
                    "text": "All the VMs from one ResourceGroup to another ResourceGroup"
                },
                {
                    "value": "A single VM migration from unmanaged to managed disks",
                    "text": "A single VM migration from unmanaged to managed disks"
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
