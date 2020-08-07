<properties
	pageTitle="Storage Files connectivity issues - Windows"
	description="Storage Files connectivity issues - Windows"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32642181"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="12748255-68F2-470D-919A-C860E861380B"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File connectivity issues - Windows
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage connectivity issues - Windows",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "What caused my Azure Files connectivity issue?",
        "description": "Our Azure Files connectivity troubleshooter can help you troubleshoot and solve your problem.",
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
            "diagnosticInputRequiredClients": "ASC"
        },
        {
            "id": "os_version",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Windows version where File Share is being mounted",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "windows7",
                    "text": "Windows 7"
                },
                {
                    "value": "windows8",
                    "text": "Windows 8 or above"
                },
                {
                    "value": "server2008R2",
                    "text": "Windows Server 2008 R2"
                },
                {
                    "value": "server2012",
                    "text": "Windows Server 2012 or above"
                },
                {
                    "value": "old_windows",
                    "text": "Below Windows 7 or Windows Server 2008 R2"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
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
            "id": "mount_error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Windows mount error",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "win_error5",
                    "text": "System error 5 has occurred. Access is denied."
                },
                {
                    "value": "win_error53",
                    "text": "System error 53 has occurred. The network path was not found."
                },
                {
                    "value": "win_error64",
                    "text": "System error 64 has occurred. The specified network name is no longer available."
                },
                {
                    "value": "win_error67",
                    "text": "System error 67 has occurred. The network name cannot be found."
                },
                {
                    "value": "win_error86",
                    "text": "System error 86 has occurred. The specified network password is not correct."
                },
                {
                    "value": "win_error87",
                    "text": "System error 87 has occurred. The parameter is incorrect."
                },
                {
                    "value": "win_error1816",
                    "text": "System error 1816 has occurred. Not enough quota is available to process this command."
                },
                {
                    "value": "win_dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_other",
            "order": 4,
            "visibility": "mount_error == win_dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Error message",
            "watermarkText": "Error message received",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
