<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32641083"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0202"
	ownershipId="Compute_VirtualMachineScaleSets"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Virtual Disk Management",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "disk_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you are getting?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "disk_add_remove",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to add or remove data disks?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Add",
                    "text": "Add"
                },
                {
                    "value": "Remove",
                    "text": "Remove"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "disk_if_vmss",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to do it on the VMSS model, or a single instance?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "VMSS",
                    "text": "VMSS"
                },
                {
                    "value": "Single Instance",
                    "text": "Single Instance"
                }
            ],
            "required": false
        },
        {
            "id": "disk_if_attachedportal",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Do you see the disks attached on the Azure Portal, but not inside the guest OS?",
            "watermarkText": "Choose an option",
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
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
