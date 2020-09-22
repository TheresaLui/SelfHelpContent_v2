<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32573480"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0088"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Unable to delete a virtual machine",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "manage_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "manage_delete",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to delete?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Only the VM",
                    "text": "Only the VM"
                },
                {
                    "value": "The entire resource group",
                    "text": "The entire resource group"
                }
            ],
            "required": false
        },
        {
            "id": "manage_isinavailabilitysetzone",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying your VM in an availability set or zone?",
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
            "id": "manage_manageddisks",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you deleting a VM with managed disks?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "manage_scenario",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "Does any of the following apply to this VM?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Have backups configured",
                    "text": "Have backups configured"
                },
                {
                    "value": "Is encrypted",
                    "text": "Is encrypted"
                },
                {
                    "value": "Has another operation running, which is pending completion",
                    "text": "Has another operation running, which is pending completion"
                },
                {
                    "value": "Someone accidentaly broke/deleted the lease on VHD",
                    "text": "Someone accidentaly broke/deleted the lease on VHD"
                },
                {
                    "value": "Is in middle of migration between resource groups or subscriptions",
                    "text": "Is in middle of migration between resource groups or subscriptions"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
