<properties
                pageTitle="Cannot Start My Virtual Machine"
                description="Cannot Start My Virtual Machine"
                authors="timbasham"
                ms.author="tibasham"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32675598"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="3b881f6a-2ca9-44e9-bab0-d9aaa2879912"
	ownershipId="Compute_VirtualMachines"
/>
# Start My VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My VM is starting",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "startstop_request",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What do you need help with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Recover my VM from a boot failure",
                    "text": "Recover my VM from a boot failure"
                },
                {
                    "value": "Recreate the Virtual Machine",
                    "text": "Recreate the Virtual Machine"
                },
                {
                    "value": "Root cause analysis",
                    "text": "Root cause analysis"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_ifnew",
            "order": 2,
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
            "order": 3,
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
            "order": 4,
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
    ]
}
---
