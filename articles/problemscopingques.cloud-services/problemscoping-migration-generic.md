<properties
                pageTitle="Migration and Move"
                description="Migration and Move"
                authors="ChiragPavecha,tanmaygore"
                ms.author="chiragpa,tagore"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32786254,32786255,32786256,32787885"
                productPesIds="13185,15660"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-migration-generic"
	ownershipId="Compute_CloudServices_Content"
/>
# CS Migration
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
                    "value": "Cloud Services(classic)",
                    "text": "Cloud Services(classic)"
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
            "required": true
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
                    "value": "Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "Azure RestAPI",
                    "text": "Azure RestAPI"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (describe below)"
                }
            ],
            "required": true
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
