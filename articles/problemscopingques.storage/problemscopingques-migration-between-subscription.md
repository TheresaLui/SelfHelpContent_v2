<properties
	pageTitle="Storage migration between subscriptions"
	description="Storage migration between subscriptions scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602699"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="66885378-3DC8-4501-BDF8-9713AE8E2CA6"
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
            "controlType": "textbox",
            "displayLabel": "Source storage account",
            "watermarkText": "Enter storage account name",
            "required": true
        },{
            "id": "storage_account_to",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Destination storage account",
            "watermarkText": "Select storage account",
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
            "watermarkText": "storage account name",
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
