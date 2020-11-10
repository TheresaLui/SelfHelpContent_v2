<properties
	pageTitle="Storage migration between subscriptions"
	description="Storage migration between subscriptions scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602699"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="66885378-3DC8-4501-BDF8-9713AE8E2CA6"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Storage migration between subscriptions
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Storage migration between subscription scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_from",
            "visibility": "true",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Source storage account",
            "watermarkText": "Select storage account name",
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
            "watermarkText": "storage account name",
            "required": true
        }, {
            "id": "storage_account_to",
            "visibility": "true",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Destination storage account",
            "watermarkText": "Enter storage account name",
	    "dropdownOptions": [
                {
                    "value": "to_new_resourcegroup_of_same_subscription",
                    "text": "To different resource group within same subscription"
                },
		 {
                    "value": "other_subscription",
                    "text": "To a different subscription"
                },
		{
                    "value": "dont_know_answer",
                    "text": "Don't know or not applicable"
                }
	],
            "required": true
        },{
            "id": "subscription_id",
            "visibility": "storage_account_to == other_subscription",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Destination subscription id",
            "watermarkText": "subscription id",
            "required": true
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
