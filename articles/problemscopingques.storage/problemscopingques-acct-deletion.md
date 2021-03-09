<properties
	pageTitle="Issue deleting storage object"
	description="Issue deleting storage object"
	authors="Leakkari"
    ms.author="leakkari"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602694"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="B01011DA-7565-4574-BD0C-35E9C749D8D1"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Issue deleting storage object
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue deleting storage object",
    "fileAttachmentHint": "",
    "formElements": [{
                "id": "service_type",
                "order": 0,
                "controlType": "dropdown",
                "displayLabel": "Type of storage object to recover",
                "watermarkText": "Choose an option",
                "dropdownOptions": [
                    {
                        "value": "rg",
                        "text": "Resource group"
                    },
                    {
                        "value": "account",
                        "text": "Storage account"
                    },
                    {
                        "value": "blob_container",
                        "text": "Blob container"
                    },
                    {
                        "value": "disk",
                        "text": "Disk"
                    },
                    {
                        "value": "blob",
                        "text": "Blob"
                    },
                    {
                        "value": "file",
                        "text": "File"
                    },
                    {
                        "value": "dont_know_answer",
                        "text": "Don't know or not listed above"
                    }
                ],
                "required": true
            },
            {
                "id": "resource_group_name",
                "order": 2,
                "visibility":"service_type == rg",
                "controlType": "textbox",
                "displayLabel": "Name of the resource group you are unable to delete",
                "watermarkText": "ResourceGroupName",
                "required": true
            },
            {
                "id":"storage_account_name",
                "order":3,
                "visibility":"service_type == account",
                "controlType":"textbox",
                "displayLabel":"Name of the storage account you are unable to delete",
                "watermarkText":"accountname1;accountname2;accountname3",
                "required":true
            },
            {
                "id": "blob_container",
                "order": 4,
                "visibility": "service_type == blob_container,
                "controlType": "textbox",
                "displayLabel": "Name of container you are unable to delete",
                "watermarkText": "container1;container2;container3",
                "required": true
            },
            {
                "id": "file",
                "order": 5,
                "visibility": "service_type == file",
                "controlType": "textbox",
                "displayLabel": "Path of file you are unable to delete",
                "watermarkText": "https://myaccount.file.core.windows.net/myfile",
                "required": true
            },
            {
            "id": "object_path",
                "order": 6,
                "visibility": "service_type == dont_know_answer",
                "controlType": "textbox",
                "displayLabel": "Path of object you are unable to delete",
                "watermarkText": "https://myaccount.file.core.windows.net/myfile",
                "required": true
            },
            {
                "id":"blob_path",
                "order":7,
                "visibility":"service_type == blob || service_type == disk",
                "controlType":"textbox",
                "displayLabel":"Blob or disk path",
                "watermarkText": "https://myaccount.blob.core.windows.net/myblob",
                "required":true
            },
            {
                "id": "error_message",
                "order": 8,
                "controlType": "multilinetextbox",
                "displayLabel": "Error message received",
                "required": false
            },
            {
                "id": "problem_description",
                "order": 9,
                "controlType": "multilinetextbox",
                "displayLabel": "Provide any additional details",
                "required": true,
                "useAsAdditionalDetails": true
            },
            {
                "id": "problem_start_time",
                "order": 10,
                "controlType": "datetimepicker",
                "displayLabel": "Problem start time",
                "required": true
            }
    ]
}
---