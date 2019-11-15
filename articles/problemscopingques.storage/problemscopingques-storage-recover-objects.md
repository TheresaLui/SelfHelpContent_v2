<properties
	pageTitle="Storage object recovery scoping"
	description="Storage object recovery scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688873"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="E6801E5C-EFBD-472A-ADC5-F21DC1C5B133"
/>
# Issues accessing a new storage account
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage object recovery",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "warning_same_name",
            "order": 0,
            "controlType": "infoblock",
            "content": "WARNING: Do not recreate storage object with the same name while we attempt to recover it."
        },
        {
            "id": "service_type",
            "order": 1,
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
                    "value": "file_share",
                    "text": "File share"
                },
                {
                    "value": "file",
                    "text": "File"
                },
                {
                    "value": "table",
                    "text": "Table"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
        {
            "id": "justification",
            "order": 2,
            "visibility": "service_type == (disk||blob||table||file_share)",
            "controlType": "multilinetextbox",
            "displayLabel": "Impact of deleted data for your business",
            "watermarkText": "Recovery of deleted data is a manual and time-consuming process. Please help us understand the business impact of the deleted data.",
            "required": false
        },
        {
            "id": "Backup method",
            "order": 3,
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
            "required": false
        },
        {
            "id": "object_path",
            "order": 4,
            "visibility": "service_type == disk || service_type == blob || service_type == table|| service_type == file",
            "controlType": "textbox",
            "displayLabel": "Path of object to recover",
            "watermarkText": "https:/{accountname}.{objectType}.core.windows.net/{objectPath}",
            "required": true
        },
        {
            "id": "object_name",
            "order": 5,
            "visibility": "service_type == account|| service_type == rg|| service_type == blob_container|| service_type == file_share",
            "controlType": "textbox",
            "displayLabel": "Name of object to recover",
            "watermarkText": "objectname1;objectname2;objectname3",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local time object was deleted",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---