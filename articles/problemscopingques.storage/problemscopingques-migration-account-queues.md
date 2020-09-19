<properties
	pageTitle="Storage migration between Storage Accounts"
	description="Storage migration between Storage Accounts scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602773"
	productPesIds="16461"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="624dabce-a5d9-4677-a069-7acfcc416e24"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Storage migration between Storage Accounts
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage migration between Storage Accounts scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "queue_names",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Queue Names",
            "watermarkText": "Select from your queues",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/queueServices/default/queues?api-version=2019-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No queues available"
                }
            }
        },
        {
            "id": "storage_account_from",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Source storage account",
            "watermarkText": "Select storage account to migrate from",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "From a different subscription, external source or not applicable"
                }
            },
            "required": true
        },{
            "id": "storage_account_from_other",
            "visibility": "storage_account_from == dont_know_answer",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Source storage account name",
            "watermarkText": "Enter storage account name",
            "required": false
        },{
            "id": "storage_account_to",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Destination storage account",
            "watermarkText": "Select storage account to migrate to",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "From a different subscription, external source or not applicable"
                }
            },
            "required": true
        },{
            "id": "storage_account_to_other",
            "visibility": "storage_account_to == dont_know_answer",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Destination storage account name",
            "watermarkText": "Enter storage account name",
            "required": false
        },{
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },{
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
