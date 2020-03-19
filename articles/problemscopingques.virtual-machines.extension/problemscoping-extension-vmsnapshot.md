<properties
                pageTitle="Virtual Machine Extensions not operating correctly"
                description="Virtual Machines Extensions not operating correctly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628288"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0051"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Agent and extensions
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "VM Snapshot (Azure Backup) extension issue",
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
            "id": "vm_extension",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select all the applicable extensions you are having issue with",
            "dynamicDropdownOptions": {
                "uri": "{resourceId}/extensions?api-version=2019-03-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of extensions.",
                    "text": "Unable to retrieve list of extensions."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "extension_operation",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What operation are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Install",
                    "text": "Install"
                },
                {
                    "value": "Uninstall",
                    "text": "Uninstall"
                },
                {
                    "value": "Enable",
                    "text": "Enable"
                },
                {
                    "value": "Troubleshoot",
                    "text": "Troubleshoot"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "extension_installed",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the extension installed?",
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
            "id": "extension_agentinstalled",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Do you have the latest Azure VM Agent installed?",
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
            "id": "extension_failure",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "What type of failure are you having?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Backup",
                    "text": "Backup"
                },
                {
                    "value": "Restore",
                    "text": "Restore"
                },
                {
                    "value": "Snapshot",
                    "text": "Snapshot"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "problem_backup_date",
            "order": 7,
            "visibility": "deployment_from == Backup",
            "controlType": "datetimepicker",
            "displayLabel": "When was the time of the attempted backup?",
            "required": true
        },
        {
            "id": "problem_restore_date",
            "order": 8,
            "visibility": "deployment_from == Restore",
            "controlType": "datetimepicker",
            "displayLabel": "When was the time of the attempted restore?",
            "required": true
        },
        {
            "id": "problem_backup_snapshot",
            "order": 9,
            "visibility": "deployment_from == Snapshot",
            "controlType": "datetimepicker",
            "displayLabel": "When was the time of the attempted snapshot?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 11,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
