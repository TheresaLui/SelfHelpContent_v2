<properties
	pageTitle="Storage migration between Storage Accounts"
	description="Storage migration between Storage Accounts scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602736,32602760,32602700,32602705,32602706"
	productPesIds="16459,16460,15629"
	cloudEnvironments="public"
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
            "displayLabel": "Destination Storage Account",
            "watermarkText": "To StorageAccountName",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
             "DropdownOptions": [
                {
                    "value": "other_subscription",
                    "text": "Storage Account from a different subscription"
                },{
                    "value": "external_source",
                    "text": "From external source"
                }
            ],
            "required": true
        },{
            "id": "storage_account_from_other_subscription",
            "visibility": "storage_account_from == other_subscription",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Storage account from a different subscription",
            "watermarkText": "From StorageAccountName",
            "required": false
        },{
            "id": "storage_account_to",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Destination Storage Account",
            "watermarkText": "To StorageAccountName",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
             "DropdownOptions": [
                {
                    "value": "other_subscription",
                    "text": "Storage account from a different subscription"
                }
            ],
            "required": true
        },{
            "id": "storage_account_to_other_subscription",
            "visibility": "storage_account_to == other_subscription",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Name of destination storage account",
            "watermarkText": "To StorageAccountName",
            "required": false
        },{
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
