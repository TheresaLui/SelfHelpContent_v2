<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32518039"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0090"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Manage encrypted disks, keys or secrets, or permissions",
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
            "id": "keyvault_access",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the KeyVault accessible within this subscription?",
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
            "id": "lost_inaccessible",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Have you lost encryption key/secret/permission or is it inaccessible?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Lost or inaccessible encryption key",
                    "text": "Lost or inaccessible encryption key"
                },
                {
                    "value": "Lost or inaccessible secret",
                    "text": "Lost or inaccessible secret"
                },
                {
                    "value": "Permission issues with Keyvault/AAD",
                    "text": "Permission issues with Keyvault/AAD"
                }
            ],
            "required": false
        },
        {
            "id": "if_aad",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you using script requiring AAD or newer version without AAD requirement?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "With AAD",
                    "text": "With AAD"
                },
                {
                    "value": "Without AAD (Newer version)",
                    "text": "Without AAD (Newer version)"
                }
            ],
            "required": false
        },
        {
            "id": "disk_encrypt",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to encrypt OS disk, data disk or all disks?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "OS disk only",
                    "text": "OS disk only"
                },
                {
                    "value": "Data disk only",
                    "text": "Data disk only"
                },
                {
                    "value": "All disks",
                    "text": "All disks"
                }
            ],
            "required": false
        },
        {
            "id": "vm_ifnew",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Is this a newly created VM or restored from backup of an encrypted VM?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Newly created VM",
                    "text": "Newly created VM"
                },
                {
                    "value": "Restoring from a backup of encrypted VM",
                    "text": "Restoring from a backup of encrypted VM"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
