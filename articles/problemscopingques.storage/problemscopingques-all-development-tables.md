<properties
	pageTitle="Development issue"
	description="Development issue for storage blob,datalake,tables and queues scoping question"
	authors="AngshumanNayakMSFT"
	ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	articleId="storagescoping_all_development-tables"
	supportTopicIds="32602772"
	productPesIds="16462"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Development and Coding Issues
---

{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Development issue on account management, blob, adlsgen2, table and queues scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "table_names",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Table Names",
            "watermarkText": "Select from your tables",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/tableServices/default/tables?api-version=2019-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No tables available"
                    }
            }
        },
        {
         "id": "problem_type",
         "order": 2,
         "controlType":"dropdown",
         "displayLabel":"How would you want us to help you?",
         "watermarkText":"Choose a problem area",
         "dropdownOptions":[
             {
             "value": "Issue",
             "text": "Troubleshoot a development/coding/scripting issue"
             },
             {
             "value": "Advisory",
             "text": "Need advisory guidance on development/coding/scripting issue"
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
            "visibility": "problem_type == Issue",
            "controlType": "datetimepicker",
            "displayLabel": "Appoximate local time of the most recent error occurrence",
            "required": true
        },
        {
            "id": "error_code_dropdown",
            "order": 4,
            "visibility": "problem_type == Issue",
            "controlType": "dropdown",
            "displayLabel": "Error code",
            "watermarkText": "HTTP error received for the failed operation",
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
                    "value": "other",
                    "text": "Not listed above  "
                }
            ],
            "required": false
        },
        {
            "id": "request_id",
            "order": 5,
            "visibility": "problem_type == Issue",
            "controlType": "textbox",
            "displayLabel": "Storage server Request ID",
            "watermarkText": "Request ID of failed operation ending with 000000",
            "textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 7,
            "controlType": "infoblock",
            "content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> issues."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
