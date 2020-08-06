<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32518038"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0080"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Encrypt virtual machine disk",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_encrypt_date",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What was the time of the attempted encryption?",
            "required": true
        },
        {
            "id": "was_encrypted",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Was this VHD encrypted earlier?",
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
            "id": "was_decrypted",
            "order": 3,
            "visibility": "was_encrypted == Yes",
            "controlType": "dropdown",
            "displayLabel": "Did you decrypt before trying encryption again?",
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
            "useAsAdditionalDetails": true,
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
