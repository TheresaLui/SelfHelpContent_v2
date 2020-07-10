<properties
                pageTitle="Migration and Move"
                description="Migration and Move"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32513964,32570114,32570115,32570116,32570117"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0103"
	ownershipId="Compute_VirtualMachines_Content"
/>
# VM Migration
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
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
            "id": "migration_resource",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "What resource(s) are you trying to migrate?",
            "watermarkText": "Choose all that applies",
            "dropdownOptions": [
                {
                    "value": "Virtual machine",
                    "text": "Virtual machine"
                },
                {
                    "value": "Availability Sets",
                    "text": "Availability Sets"
                },
                {
                    "value": "Cloud Services with Virtual Machines",
                    "text": "Cloud Services with Virtual Machines"
                },
                {
                    "value": "Storage Accounts",
                    "text": "Storage Accounts"
                },
                {
                    "value": "Virtual Networks",
                    "text": "Virtual Networks"
                },
                {
                    "value": "VPN Gateways",
                    "text": "VPN Gateways"
                },
                {
                    "value": "Express Route Gateways",
                    "text": "Express Route Gateways"
                },
                {
                    "value": "Network Security Groups",
                    "text": "Network Security Groups"
                },
                {
                    "value": "Route Tables",
                    "text": "Route Tables"
                },
                {
                    "value": "Reserved IPs",
                    "text": "Reserved IPs"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": false
        },
        {
            "id": "migration_ifvnet",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you migrating the resource in a vNet?",
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
            "id": "migration_method",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "How did you perform the migration?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "PowerShell",
                    "text": "PowerShell"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "AsmMetadataParser",
                    "text": "AsmMetadataParser"
                },
                {
                    "value": "migAz",
                    "text": "migAz"
                },
                {
                    "value": "Azure Portal",
                    "text": "Azure Portal"
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
