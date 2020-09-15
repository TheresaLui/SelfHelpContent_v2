<properties
	pageTitle="Storage File Share mounting issues - Linux"
	description="Storage File Share mounting issues - Linux"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602763"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="79f6826d-4649-4cd1-bb10-5ea01b616d3d"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File Share mounting issues - Linux
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File Share mounting issues - Linux",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "What caused my Azure Files mount issue on Linux?",
        "description": "Our Azure Files mount troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure that File Share or File Path provided is in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "file_share_or_path",
            "order": 0,
            "controlType": "textbox",
            "displayLabel": "File Share or File path",
            "watermarkText": "'FileShare' or 'FileShare/FileName'",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "file_share_protocol",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "File Share Protocol",
            "watermarkText": "Select File Share Protocol",
            "dropdownOptions": [
                {
                    "value": "SMB",
                    "text": "SMB Protocol"
                },
                {
                    "value": "NFS",
                    "text": "NFS Protocol"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "mount_location",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Location where File Share is being mounted",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "same_region",
                    "text": "Azure VM is in same region as the Azure File Share"
                },
                {
                    "value": "different_region",
                    "text": "Azure VM is in different region than the Azure File Share"
                },
                {
                    "value": "on_premises",
                    "text": "Client is outside Azure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "os_version",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Linux version where File Share is being mounted",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Ubuntu_below1404",
                    "text": "Ubuntu Server below 14.04"
                },
                {
                    "value": "Ubuntu_1404_1510",
                    "text": "Ubuntu Server 14.04 - 15.10"
                },
                {
                    "value": "Ubuntu_above1604",
                    "text": "Ubuntu Server 16.04 or above"
                },
                {
                    "value": "rhel_below7",
                    "text": "RHEL below 7"
                },
                {
                    "value": "rhel_7_74",
                    "text": "RHEL 7.0 - 7.4"
                },
                {
                    "value": "rhel_above75",
                    "text": "RHEL 7.5 or above"
                },
                {
                    "value": "CentOS_below7",
                    "text": "CentOS below 7"
                },
                {
                    "value": "CentOS_7_74",
                    "text": "CentOS 7.0 - 7.4"
                },
                {
                    "value": "CentOS_above75",
                    "text": "CentOS 7.5 or above"
                },
                {
                    "value": "Debian_below8",
                    "text": "Debian below 8"
                },
                {
                    "value": "Debian_above8",
                    "text": "Debian 8 or above"
                },
                {
                    "value": "OpenSUSE_below132",
                    "text": "OpenSUSE below 13.2"
                },
                {
                    "value": "OpenSUSE_132_422",
                    "text": "OpenSUSE 13.2 - 42.2"
                },
                {
                    "value": "OpenSUSE_above423",
                    "text": "OpenSUSE 42.3 or above"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other - provide Linux kernel version below"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "linux_kernel",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Linux kernel version",
            "watermarkText": "Run 'uname -r' command to find Linux kernel version",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "mount_error",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Linux mount error",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "linux_error2",
                    "text": "Mount error(2): No such file or directory"
                },
                {
                    "value": "linux_error11",
                    "text": "Mount error(11): Resource temporarily unavailable"
                },
                {
                    "value": "linux_error13",
                    "text": "Mount error(13): Permission denied"
                },
                {
                    "value": "linux_error22",
                    "text": "Mount error(22): Invalid argument"
                },
                {
                    "value": "linux_error112",
                    "text": "Mount error(112): Host is down"
                },
                {
                    "value": "linux_error115",
                    "text": "Mount error(115): Operation now in progress"
                },
                {
                    "value": "linux_dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_other",
            "order": 6,
            "visibility": "mount_error == linux_dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Error message",
            "watermarkText": "Error message received",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
