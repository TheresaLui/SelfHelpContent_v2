<properties
                pageTitle="Cannot Start or Stop My Virtual Machine"
                description="Cannot Start or Stop My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628285"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0008"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Start or Stop My VM
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My VM will not start after a configuration change",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "startstop_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "startstop_config",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What was your configuration change prior to the issue starting?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I resized my virtual machine",
                    "text": "I resized my virtual machine"
                },
                {
                    "value": "I attached or detached disks",
                    "text": "I attached or detached disks"
                },
                {
                    "value": "I moved my VM to another network/subnet or resource group",
                    "text": "I moved my VM to another network/subnet or resource group"
                },
                {
                    "value": "I changed my firewall configuration",
                    "text": "I changed my firewall configuration"
                },
                {
                    "value": "I installed a third party application",
                    "text": "I installed a third party application"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_config_other",
            "order": 3,
            "visibility": "startstop_config == Other",
            "controlType": "multilinetextbox",
            "displayLabel": "Please specify your configuration change prior to the issue starting.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "startstop_ifnew",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is this VM new to Azure?",
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
            "id": "startstop_from",
            "order": 5,
            "visibility": "startstop_ifnew == Yes",
            "controlType": "dropdown",
            "displayLabel": "Where is the VM from?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "On premise",
                    "text": "On premise"
                },
                {
                    "value": "From ASM to ARM",
                    "text": "From ASM to ARM"
                },
                {
                    "value": "From another cloud provider",
                    "text": "From another cloud provider"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_ifazuresiterecovery",
            "order": 6,
            "visibility": "startstop_from == On premise || startstop_from == From another cloud provider",
            "controlType": "dropdown",
            "displayLabel": "How was this machine migrated?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I used Azure Site Recovery",
                    "text": "I used Azure Site Recovery"
                },
                {
                    "value": "I used a third-party migration tool",
                    "text": "I used a third-party migration tool"
                },
                {
                    "value": "I uploaded the disk manually",
                    "text": "I uploaded the disk manually"
                },
                {
                    "value": "I used Azure Migrate",
                    "text": "I used Azure Migrate"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_ifbackup",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Was this VM recovered from backup?",
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
            "id": "startstop_ifinternet",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Do you have Internet connectivity issues from this VM?",
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
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
