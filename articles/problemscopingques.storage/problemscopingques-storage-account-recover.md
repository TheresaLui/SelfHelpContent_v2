<properties
	pageTitle="Recover deleted Storage Account"
	description="Recover deleted Storage Account scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602701,32642178"
	productPesIds="15629,16459"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="2165ec52-93b8-4bad-bf52-2b24b8f186cf"
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
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Date and time that the account was deleted",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 7,
            "controlType": "infoblock",
            "content": "You can follow our <a href='https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data'>best practices for protecting your data</a> to ensure that your deleted data will be recoverable in the future."
        }
    ],
    "$schema": "SelfHelpContent"
}
---