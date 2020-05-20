<properties
	pageTitle="Storage account access issues"
	description="Issues accessing new storage account scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688875"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="C3E60F52-8476-4DE4-9146-0BE3DC49ECEB"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Issues accessing a new storage account
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage account access issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_name",
            "order": 0,
            "controlType": "textbox",
            "displayLabel": "Name of storage account with access issue",
            "required": false
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message received",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time of most recent occurrence",
            "required": true
        },
        {
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