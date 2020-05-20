<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615531"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0016"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Connect to a VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My problem is not listed above",
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
            "id": "connect_config",
            "order": 2,
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
            "id": "connect_config_firewall",
            "order": 3,
            "visibility": "connect_config == I've changed my firewall configuration",
            "controlType": "dropdown",
            "displayLabel": "What type of changes were done?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I've followed Security Center recommendations",
                    "text": "I've followed Security Center recommendations"
                },
                {
                    "value": "I've applied OS hardening",
                    "text": "I've applied OS hardening"
                }
            ],
            "required": false
        },
        {
            "id": "connect_config_other",
            "order": 4,
            "visibility": "connect_config == Other",
            "controlType": "multilinetextbox",
            "displayLabel": "Please specify your configuration change prior to the issue starting.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "ippublicprivate",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Do you have issues connecting via Public or Private IP?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Public IP",
                    "text": "Public IP"
                },
                {
                    "value": "Private IP",
                    "text": "Private IP"
                },
                {
                    "value": "Azure Bastion",
                    "text": "Azure Bastion"
                }
            ],
            "required": false
        },
        {
            "id": "ippublic",
            "order": 6,
            "visibility": "ippublicprivate == Public IP",
            "controlType": "dropdown",
            "displayLabel": "Are you able to connect to the Private IP?",
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
            "id": "ipprivate",
            "order": 7,
            "visibility": "ippublicprivate == Private IP",
            "controlType": "dropdown",
            "displayLabel": "Are you able to connect to the Public IP?",
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
                    "value": "I don't have a Public IP",
                    "text": "I don't have a Public IP"
                }
            ],
            "required": false
        },
        {
            "id": "connect_subnet",
            "order": 8,
            "visibility": "ippublic == No || ipprivate == No || ipprivate == I don't have a Public IP",
            "controlType": "dropdown",
            "displayLabel": "Is the problem isolated when you are connecting from a specific subnet?",
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
            "id": "bastionresource",
            "order": 9,
            "visibility": "ippublicprivate == Azure Bastion",
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
            "order": 10,
            "visibility": "ippublicprivate == Azure Bastion",
            "controlType": "textbox",
            "displayLabel": "What browser are you using?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "bastionbrowserversion",
            "order": 11,
            "visibility": "ippublicprivate == Azure Bastion",
            "controlType": "textbox",
            "displayLabel": "What version is your browser?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "bastionbrowseros",
            "order": 12,
            "visibility": "ippublicprivate == Azure Bastion",
            "controlType": "textbox",
            "displayLabel": "What OS is your browser running in?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "isadmin",
            "order": 13,
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
            "order": 14,
            "visibility": "isadmin == No || isadmin == I do not know",
            "controlType": "textbox",
            "displayLabel": "What is the name of the user account trying to login?",
            "required": false
        },
        {
            "id": "connect_ifnew",
            "order": 15,
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
            "order": 16,
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
            "order": 17,
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
            "order": 18,
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
            "id": "connect_ifbackup",
            "order": 19,
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
            "id": "connect_ifinternet",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Do you have connectivity issues from/to this VM?",
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
            "id": "connect_internetissue",
            "order": 21,
            "visibility": "connect_ifinternet == Yes",
            "controlType": "dropdown",
            "displayLabel": "What is the problem you are having?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Cannot connect to the RDP port",
                    "text": "Cannot connect to the RDP port"
                },
                {
                    "value": "Cannot connect to the Powershell port",
                    "text": "Cannot connect to the Powershell port"
                },
                {
                    "value": "Cannot connect to my SQL instance",
                    "text": "Cannot connect to my SQL instance"
                },
                {
                    "value": "Cannot connect to another port",
                    "text": "Cannot connect to another port"
                },
                {
                    "value": "My VM doesn't have access to Internet",
                    "text": "My VM doesn't have access to Internet"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 22,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 23,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
