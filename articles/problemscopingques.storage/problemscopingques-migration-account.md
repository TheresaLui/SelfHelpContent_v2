<properties
	pageTitle="Storage migration between Storage Accounts"
	description="Storage migration between Storage Accounts scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602736,32602700,32602705,32602706,32602773"
	productPesIds="16459,15629,16461,16462"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="db69e7ff-4d73-423a-97ae-b30cee9f0d64"
/>
# Storage migration between Storage Accounts
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Storage migration between Storage Accounts scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_from",
            "order": 1,
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
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Source storage account name",
            "watermarkText": "Enter storage account name",
            "required": false
        },{
            "id": "storage_account_to",
            "order": 3,
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
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Destination storage account name",
            "watermarkText": "Enter storage account name",
            "required": false
        },{
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },{
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
