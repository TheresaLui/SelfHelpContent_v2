<properties
	pageTitle="Storage File Share connectivity issues - macOS"
	description="Storage File Share connectivity issues - macOS"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32642180"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="3EB210D0-F208-463E-9A67-4357829706A9"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File Share connectivity issues - macOS
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File Share mounting issues - macOS",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "What caused my Azure Files connectivity issue on MacOS?",
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
            "displayLabel": "MacOS version where File Share is being mounted",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "OSX_above1011",
                    "text": "El Capitan (version 10.11) or above"
                },
                {
                    "value": "OSX_below1010",
                    "text": "Yosemite (version 10.10) or below"
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
