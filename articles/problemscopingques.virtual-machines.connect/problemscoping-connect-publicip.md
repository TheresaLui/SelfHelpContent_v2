<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615527"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0018"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Connect to a VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "I have an issue with my public IP",
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
            "id": "connect_ifnew",
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
            "id": "connect_from",
            "order": 3,
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
            "order": 4,
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
            "order": 5,
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
            "id": "machinetype",
            "order": 6,
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
            "id": "ippublic",
            "order": 7,
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
            "id": "connect_subnet",
            "order": 8,
            "visibility": "ippublic == No",
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
            "id": "connect_ifinternet",
            "order": 9,
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
            "order": 10,
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
            "order": 11,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 12,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
