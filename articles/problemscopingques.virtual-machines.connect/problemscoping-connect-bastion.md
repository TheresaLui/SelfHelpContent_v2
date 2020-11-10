<properties
    pageTitle="Cannot Connect to My Virtual Machine using Azure Bastion"
    description="Cannot Connect to My Virtual Machine using Azure Bastion"
    authors="timbasham"
    ms.author="tibasham"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32663940"
    productPesIds="14749"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="a5907259-3329-4b6f-8a82-310965520f9d"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Connect to a VM using Azure Bastion
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Failure to connect to the VM using Azure Bastion",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "bastionresource",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select your Azure Bastion resource",
            "watermarkText": "Choose a resource",
            "required": false,
            "dynamicDropdownOptions": {
                    "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Network/bastionHosts?api-version=2019-04-01",
                    "jTokenPath": "value",
                    "textProperty": "name",
                    "valueProperty": "id",
                    "textPropertyRegex": "[^/]+$",
                    "defaultDropdownOptions": {
                        "value": "dont_know_answer",
                        "text": "Other, don't know or not applicable"
                    }
            }
        },
        {
            "id": "bastionbrowser",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What browser are you using?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "bastionbrowserversion",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What version is your browser?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "bastionbrowseros",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What OS is your browser running in?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "isadmin",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Is this the built-in administrator account?",
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
            "id": "name_useraccount",
            "order": 7,
            "visibility": "isadmin == No || isadmin == I do not know",
            "controlType": "textbox",
            "displayLabel": "What is the name of the user account trying to login?",
            "required": false
        },
        {
            "id": "connect_ifnew",
            "order": 8,
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
            "id": "connect_from",
            "order": 9,
            "visibility": "connect_ifnew == Yes",
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
                },
                {
                        "value": "Azure Marketplace",
                        "text": "Azure Marketplace"
                }
            ],
            "required": false
        },
        {
            "id": "connect_howmigrated",
            "order": 10,
            "visibility": "connect_from == On premise || connect_from == From another cloud provider",
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
            "id": "connect_wasoncloud",
            "order": 11,
            "visibility": "connect_from == On premise",
            "controlType": "dropdown",
            "displayLabel": "Was the machine prepared to work on a cloud environment prior the migration?",
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
            "id": "connect_config",
            "order": 12,
            "controlType": "dropdown",
            "displayLabel": "Please specify your configuration change prior to the issue starting",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I've changed my VM size",
                    "text": "I've changed my VM size"
                },
                {
                    "value": "I've made a disk change (attach, detach, resize)",
                    "text": "I've made a disk change (attach, detach, resize)"
                },
                {
                    "value": "I've modified network parameters on my VM (DNS, Ips, routing tables, etc)",
                    "text": "I've modified network parameters on my VM (DNS, Ips, routing tables, etc)"
                },
                {
                    "value": "I've changed my firewall configuration",
                    "text": "I've changed my firewall configuration"
                },
                {
                    "value": "I've installed a 3rd party app (Antivirus, firewall, VPN client, etc)",
                    "text": "I've installed a 3rd party app (Antivirus, firewall, VPN client, etc)"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "machinetype",
            "order": 13,
            "controlType": "dropdown",
            "displayLabel": "From which type of machine are you trying to RDP into?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows 7/Windows Server 2008R2",
                    "text": "Windows 7/Windows Server 2008R2"
                },
                {
                    "value": "Windows 8/Windows Server 2012",
                    "text": "Windows 8/Windows Server 2012"
                },
                {
                    "value": "Windows 8.1/Windows Server 2012R2",
                    "text": "Windows 8.1/Windows Server 2012R2"
                },
                {
                    "value": "Windows 10/Windows Server 2016",
                    "text": "Windows 10/Windows Server 2016"
                },
                {
                    "value": "Windows 10/Windows Server 2019",
                    "text": "Windows 10/Windows Server 2019"
                },
                {
                    "value": "Android or iOS",
                    "text": "Android or iOS"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 14,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 15,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ]
}
---
