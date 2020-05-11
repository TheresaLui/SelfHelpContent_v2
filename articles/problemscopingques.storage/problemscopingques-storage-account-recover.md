<properties
	pageTitle="Recover deleted Storage Account"
	description="Recover deleted Storage Account scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602701"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="2165ec52-93b8-4bad-bf52-2b24b8f186cf"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Recover deleted Storage Account
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Storage account recovery scoping questions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Is it possible to recover my deleted storage account?",
        "description": "Our storage account recovery troubleshooter can help identify if it is possible to recover your deleted account",
        "insightNotAvailableText": "Our troubleshooter could not identify if your deleted account is recoverable or not. Please ensure that the storage account name provided is correct."
    },
    "formElements": [
        {
            "id": "warning_same_name",
            "order": 1,
            "controlType": "infoblock",
            "content": "WARNING: Do not recreate Storage Account with the same name while we attempt to recover it."
        },
        {
            "id": "storage_account_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Name of the deleted Storage Account",
            "watermarkText": "accountname1;accountname2;accountname3",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Date and time that the account was deleted",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
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