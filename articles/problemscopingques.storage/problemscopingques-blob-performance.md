<properties
	pageTitle="Performance issue on blob"
	description="Performance issue on blob and adls scoping question"
	authors="annayak"
    ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602726,32602727,32612602,32612604"
	productPesIds="16459,16598"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="51f6b586-c2a9-4744-b7d3-8f01cef66201"
/>
# Blob and ADLS performance issue
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance issue on blob scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What type of issue are you reporting?",
            "watermarkText": "Choose an issue type",
             "dropdownOptions": [
                {
                    "value": "Issue",
                    "text": "Issue"
                },
                {
                    "value": "Advisory",
                    "text": "Advisory"
                },
                {
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
            ],
            "required": true
            },        
        {
            "id": "issue_nature",
            "order": 2,
            "visibility": "problem_type == Issue",
            "controlType": "dropdown",
            "displayLabel": "Is it ongoing or happened in past?",
            "watermarkText": "Choose whether it's currently ongoing or happend in past and resolved",
             "dropdownOptions": [
                {
                    "value": "Issue_Ongoing",
                    "text": "Reporting an ongoing performance issue"
                },
                {
                    "value": "Issue_Resolved",
                    "text": "Need root cause for a resolved performance issue"
                },
                {
                    "value": "dont_know_answer",
                    "text": "None of the above"
                    }              
            ],
            "required": true
            },           
        {
            "id": "problem_start_time",
            "order": 3,
            "visibility": "issue_nature == Reporting an ongoing performance issue || issue_nature == Need root cuase for a resolved performance issue",
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local start time of the most recent occurrence",
            "required": true
            },
        {
            "id": "problem_end_time",
            "order": 4,
            "visibility": "issue_nature == Need root cuase for a resolved performance issue",
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local end time of the most recent occurrence. Enter current time if the performance issue is still continuing",
            "required": true
            },
        {
            "id": "request_id",
            "order": 5,
            "visibility": "issue_nature == Reporting an ongoing performance issue || issue_nature == Need root cuase for a resolved performance issue",
            "controlType": "textbox",
            "displayLabel": "Storage server Request ID",
            "watermarkText": "Request ID of failed operation ending with 000000",
            "textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
            "required": true
            },
        {
            "id": "error_code_dropdown",
            "order": 6,
            "visibility": "issue_nature == Reporting an ongoing performance issue || issue_nature == Need root cuase for a resolved performance issue",
            "controlType": "dropdown",
            "displayLabel": "Error code",
            "watermarkText": "HTTP error of failed operation",
            "dropdownOptions": [
                {
                    "value": "HTTP_401",
                    "text": "HTTP 401"
                },
                {
                    "value": "HTTP_403",
                    "text": "HTTP 403"
                },
                {
                    "value": "HTTP_409",
                    "text": "HTTP 409"
                },
                {
                    "value": "HTTP_500",
                    "text": "HTTP 500"
                },
                {
                    "value": "HTTP_503",
                    "text": "HTTP 503"
                },
                {
                    "value": "other",
                    "text": "Not listed above  "
                }
            ],
            "required": true
            },
        {
            "id": "blob_container",
            "order": 7,
            "visibility": "issue_nature == Reporting an ongoing performance issue || issue_nature == Need root cuase for a resolved performance issue",
            "controlType": "dropdown",
            "displayLabel": "Blob Container",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/default/containers?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoBlobContainer",
                    "text": "Not specific to a blob container"
                }
            ],
            "required": false
        },
        {
            "id": "blob_path",
            "order": 8,
            "visibility": "issue_nature == Reporting an ongoing performance issue || issue_nature == Need root cuase for a resolved performance issue",
            "controlType": "textbox",
            "displayLabel": "Blob path",
            "watermarkText": "Blob name or path if specific to a blob",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details like error message or exception stack",
            "required": true,
            "useAsAdditionalDetails": true
        },        
        {
            "id": "learn_more_text",
            "order": 10,
            "controlType": "infoblock",
            "content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> to troubleshoot performance issues."
        }
    ],
    "$schema": "SelfHelpContent"
}
---