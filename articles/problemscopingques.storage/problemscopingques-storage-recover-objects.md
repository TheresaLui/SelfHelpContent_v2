<properties
	pageTitle="Storage object recovery scoping"
	description="Storage object recovery scoping question"
	authors="Sijia"
    	ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688873,32642178"
	productPesIds="15629,16459"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="E6801E5C-EFBD-472A-ADC5-F21DC1C5B133"
    	ownershipId="StorageMediaEdge_XStore"
/>
# Issues accessing a new storage account
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage object recovery",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to check if storage resource is recoverable?",
        "description": "Our Azure Storage diagnostics can help you find out if the storage resource is recoverable. Please fill in the information below to find an answer.",
        "insightNotAvailableText": "Our diagnostics did not find your storage resource. Please ensure the information provided is accurate and in the approved format. Also, check recommended solution below to find an answer."
	},
    "formElements": [
        {
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
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "resource_group_name",
            "order": 2,
            "visibility":"service_type == rg",
            "controlType": "textbox",
            "displayLabel": "Name of the deleted resource group",
            "watermarkText": "ResourceGroupName",
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id":"recovery_type",
            "order":3,
            "visibility":"service_type == rg",
            "controlType":"dropdown",
            "displayLabel":"We can only attempt to recover deleted stroage accounts in this Resource Group. Do you want us to attempt to recover them?",
            "watermarkText":"Choose an option",
            "dropdownOptions":[
                {
                    "value":"yes",
                    "text":"Yes, attempt to recover all storage accounts in resource group above"
                },
                {
                    "value":"some_accounts",
                    "text":"Only attempt to recover some storage accounts in resource group above"
                },
                {
                    "value":"no",
                    "text":"No, I do not want to recover any storage accounts"
                },
                {
                    "value":"dont_know_answer",
                    "text":"Other, don't know or not applicable"
                }
            ],
            "required":true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id":"storage_account_name",
            "order":4,
            "visibility":"service_type == account",
            "controlType":"textbox",
            "displayLabel":"Name of the deleted storage account to recover",
            "watermarkText":"accountname1;accountname2;accountname3",
            "required":true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id":"recovery_option",
            "order":5,
            "visibility":"service_type == blob_container",
            "controlType":"dropdown",
            "displayLabel":"Recovery Option",
            "watermarkText":"Choose an option",
            "dropdownOptions":[
                {
                    "value":"by_container_name",
                    "text":"Recover by container name"
                },
                {
                    "value":"by_time_period",
                    "text":"Recover by deleted time period"
                },
                {
                    "value":"dont_know_answer",
                    "text":"Other, don't know or not applicable"
                }
            ],
            "required":true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "blob_container",
            "order": 6,
            "visibility": "service_type == blob_container && recovery_option == by_container_name",
            "controlType": "textbox",
            "displayLabel": "Name of container to recover",
            "watermarkText": "container1;container2;container3",
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "object_name",
            "order": 7,
            "visibility": "service_type == file_share || service_type == table",
            "controlType": "textbox",
            "displayLabel": "Name of object to recover",
            "watermarkText": "objectname1;objectname2;objectname3",
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "object_path",
            "order": 10,
            "visibility": "service_type == file || service_type == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Path of object to recover",
            "watermarkText": "https://myaccount.file.core.windows.net/myfile",
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id":"blob_path",
            "order":11,
            "visibility":"service_type == blob || service_type == disk",
            "controlType":"textbox",
            "displayLabel":"Blob or disk path",
            "watermarkText": "https://myaccount.blob.core.windows.net/myblob",
            "required":true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "Backup method",
            "order": 12,
            "visibility": "service_type == file",
            "controlType": "dropdown",
            "displayLabel": "Backup method",
            "watermarkText": "It is not possible to recover deleted Azure Files without backup",
                        "dropdownOptions": [
                {
                    "value": "snapshots",
                    "text": "Snapshots"
                },
                {
                    "value": "azure_backup",
                    "text": "Azure Backup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "data_type",
            "order": 14,
            "visibility": "service_type == disk||service_type == blob||service_type == table)",
            "controlType": "dropdown",
            "displayLabel": "Type of data",
            "watermarkText": "Type of data you wish to recover",
                        "dropdownOptions": [
                {
                    "value": "production",
                    "text": "Production data"
                },
                {
                    "value": "test",
                    "text": "Test data"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "justification",
            "order": 15,
            "visibility": "service_type == disk||service_type == blob||service_type == table) ",
            "controlType": "multilinetextbox",
            "displayLabel": "Impact of deleted data for your business",
            "watermarkText": "Recovery of deleted data is a manual and time-consuming process. Please help us understand the business impact of the deleted data.",
            "required": false,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 17,
            "controlType": "datetimepicker",
            "displayLabel": "Local start time when object was deleted",
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_end_time",
            "order": 18,
            "visibility": "service_type == blob_container && recovery_option == by_time_period",
            "controlType": "datetimepicker",
            "displayLabel": "Local end time when object was deleted",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 19,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
       
