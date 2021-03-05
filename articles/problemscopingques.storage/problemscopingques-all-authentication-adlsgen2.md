<properties
	pageTitle="Authentication and Authorization Issue"
	description="Authentication and Authorization issue for adlsgen2 scoping question"
	authors="AngshumanNayakMSFT"
	ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	articleId="StorageScoping_all_authentication"
	supportTopicIds="32679291,32679292,32679290,32680499,32731237"
	productPesIds="16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Authentication and Authorization Issue
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Authentication and Authorization issue for adlsgen2 scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Authentication Issues Troubleshooter",
        "description": "If you are reporting about an issue please help us with a few inputs and give us a few minutes to run automated diagnostics. We can help you to diagnose your issue without opening a support ticket.",
        "insightNotAvailableText": "Our automated troubleshooter did not detect any issues with your resource. You can help us by providing the right inputs below and ensuring that the format is as suggested in the watermark."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Local start time of the latest occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_code_dropdown",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Error code",
            "watermarkText": "HTTP error of failed operation",
            "defaultDropdownOptions": "HTTP 403",
	    "infoBalloonText":"Select the HTTP error of the failed operation",
            "dropdownOptions": [
                {
                    "value": "HTTP_304",
                    "text": "HTTP 304"
                },
                {
                    "value": "HTTP_400",
                    "text": "HTTP 400"
                },
                {
                    "value": "HTTP_403",
                    "text": "HTTP 403"
                },
                {
                    "value": "HTTP_404",
                    "text": "HTTP 404"
                },
                {
                    "value": "HTTP_405",
                    "text": "HTTP 405"
                },
                {
                    "value": "HTTP_409",
                    "text": "HTTP 409"
                },
                {
                    "value": "HTTP_411",
                    "text": "HTTP 411"
                },
                {
                    "value": "HTTP_412",
                    "text": "HTTP 412"
                },
                {
                    "value": "HTTP_413",
                    "text": "HTTP 413"
                },
                {
                    "value": "HTTP_415",
                    "text": "HTTP 415"
                },
                {
                    "value": "HTTP_416",
                    "text": "HTTP 416"
                },
                {
                    "value": "HTTP_500",
                    "text": "HTTP 500"
                },
                {
                    "value": "HTTP_501",
                    "text": "HTTP 501"
                },
                {
                    "value": "HTTP_502",
                    "text": "HTTP 502"
                },
                {
                    "value": "HTTP_503",
                    "text": "HTTP 503"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not listed above"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "request_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Storage server request ID",
            "watermarkText": "Server Request ID of failed operation ending with 000000",
	    "infoBalloonText":"Server Request ID of failed operation ending with 000000(6 zeros). This is part of every response that is sent back by storage.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC",
	    "validations": [
		{
		    "type": "RegExMatch",
		    "value": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
		    "text": "Server Request ID always ends 000000(6 zeros) e.g 05b2d321-403q-0037-4f62-2ag1aa000000"
		}
	    ]
        },
        {
            "id": "blob_container",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Blob container",
            "watermarkText": "Choose a specific container",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/default/containers?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": { "value": "dont_know_answer",
                "text": "None of the above"
                }
            },
            "dropdownOptions": [
                {
                    "value": "NoBlobContainer",
                    "text": "Not specific to a blob container"
                }
            ],
            "required": false,
             "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "blob_path",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Blob path",
            "watermarkText": "Blob name or path if specific to a blob",
            "required": false,
             "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "learn_more_text",
            "order": 7,
            "controlType": "infoblock",
            "content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> performance issues."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
