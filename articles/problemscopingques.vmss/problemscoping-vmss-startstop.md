<properties
                pageTitle="My instance was restarted or stopped unexpectedly"
                description="My instance was restarted or stopped unexpectedly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32641073"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0111"
	ownershipId="Compute_VirtualMachineScaleSets"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "My instance was restarted or stopped unexpectedly",
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
                    "value": "I resized my virtual machine scale set",
                    "text": "I resized my virtual machine scale set"
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
            "displayLabel": "Is this VMSS new to Azure?",
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
            "id": "startstop_ifbackup",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Was this VMSS recovered from backup?",
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
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Do you have Internet connectivity issues from this VMSS?",
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
            "id": "startstop_issue",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "What is the issue you are experiencing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Unexpected restart of the VMs",
                    "text": "Unexpected restart of the VMs"
                },
                {
                    "value": "Unresponsiveness of the VMs",
                    "text": "Unresponsiveness of the VMs"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_ifone",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Did the issue affected one VM or all the instances of the VMSS?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "One VM",
                    "text": "One VM"
                },
                {
                    "value": "All the instances",
                    "text": "All the instances"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_single_vm",
            "order": 9,
            "visibility": "startstop_ifone == One VM",
            "controlType": "textbox",
            "displayLabel": "Please specify the affected instance.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "startstop_rca_fix",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "Are you requesting a fix or an RCA?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "RCA",
                    "text": "RCA"
                },
                {
                    "value": "Fix",
                    "text": "Fix"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 11,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
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
