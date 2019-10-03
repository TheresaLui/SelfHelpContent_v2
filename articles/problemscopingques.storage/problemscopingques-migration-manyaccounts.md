<properties
	pageTitle="How to choose data migration solution"
	description="How to choose data migration solution"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32634987,32605567"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="ED05B7F3-35E8-4F28-B3A3-FBFF20E2B301"
/>

# Storage migration between Storage Accounts
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "How to choose data migration solution",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_from",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Storage accounts from",
            "watermarkText": "AccountName1;AccountName2;AccountName3",
            "required": true
        },
	{
            "id": "storage_account_to",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Storage account to",
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
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Destination storage account name",
            "watermarkText": "Enter storage account name",
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
