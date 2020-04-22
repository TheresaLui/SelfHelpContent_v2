<properties
	pageTitle="Recover deleted resource group"
	description="Recover deleted resource group scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32642177"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="E7F354E1-8263-43BD-9D01-2AAAF1C6316F"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Recover deleted Resource Group
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Resource group recovery scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Is it possible to recover storage account(s)in deleted resource group?",
        "description": "Our storage account recovery troubleshooter can help identify if it is possible to recover storage account(s) in your deleted resource group",
        "insightNotAvailableText": "Our troubleshooter could not identify if your account(s) in deleted resource group is recoverable or not. Please ensure that the resource group name provided is correct."
    },
    "formElements": [
        {
            "id": "warning_same_name",
            "order": 1,
            "controlType": "infoblock",
            "content": "WARNING: We will attempt to recover deleted storage accounts in this resource group. Do not recreate storage accounts with the same name while we attempt to recover them."
        },
        {
            "id": "resource_group_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Name of the deleted resource group",
            "watermarkText": "ResourceGroupName",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "recovery_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "We can only attempt to recover deleted stroage accounts in this Resource Group. Do you want us to attempt to recover them?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes, attempt to recover all storage accounts in resource group above"
                },
                {
                    "value": "some_accounts",
                    "text": "Only attempt to recover some storage accounts in resource group above"
                },
                {
                    "value": "no",
                    "text": "No, I do not want to recover any storage accounts"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "storage_accounts",
            "order": 4,
            "visibility": "recovery_type == some_accounts",
            "controlType": "multilinetextbox",
            "displayLabel": "Name of storage accounts to recover",
            "watermarkText": "accountname1;accountname2;accountname3",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Date and time that the resource group was deleted",
            "required": true
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