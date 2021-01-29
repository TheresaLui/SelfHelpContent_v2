<properties
                pageTitle="Azure Disk Encryption not operating correctly"
                description="Azure Disk Encryption not operating correctly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32743903"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0241"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Agent and extensions
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issue with Server Side Encryption",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "extension_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "ade_issue",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What are you having an issue with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Server Side encryption using PMK",
                    "text": "Server Side encryption using PMK"
                },
                {
                    "value": "Server side encryption using CMK",
                    "text": "Server side encryption using CMK"
                },
                {
                    "value": "Encryption at host",
                    "text": "Encryption at host"
                },
                {
                    "value": "Double Encryption at Rest",
                    "text": "Double Encryption at Rest"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "ade_vm",
            "order": 3,
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
            "id": "ade_if_change_encryption_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to change the encryption type on your disk?",
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
