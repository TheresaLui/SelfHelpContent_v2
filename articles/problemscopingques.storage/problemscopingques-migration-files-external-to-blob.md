<properties
	pageTitle="Transfer data from external sources to Blob storage"
	description="Issues with transferring data from external sources to Blob storage"
	authors="Sijia"
  ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32612614"
	productPesIds="16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="b32ffb32-eb2f-4302-8261-212ea82ca36c"
	ownershipId="StorageMediaEdge_DataLakeStorageGen2"
/>

# Transfer data from external sources to Blob storage
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "How to choose data migration solution",
    "fileAttachmentHint": "",
    "formElements": [
	      {
            "id": "azcopy_command_needhelp",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have questions on AzCopy command",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "yes"
                },
                {
                    "value": "no",
                    "text": "no"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": false
        },
        {
            "id": "azcopy_performance",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you experiencing any performance issue with the copy operations",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
        {
            "id": "error_code",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you receive any error code? ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "error400",
                    "text": "400 - Bad Request"
                },
                {
                    "value": "error401",
                    "text": "401 – Unauthorized"
                },
                {
                    "value": "error403",
                    "text": "403 – Forbidden"
                },
                {
                    "value": "error404",
                    "text": "404 - Resource not found (Authentication)"
                },
                {
                    "value": "error409",
                    "text": "409 - Conflict"
                },
                {
                    "value": "error412",
                    "text": "412 – Precondition failed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
