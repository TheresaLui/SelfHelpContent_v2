<properties
	pageTitle="Recover deleted resource group"
	description="Recover deleted resource group scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32642177"
	productPesIds="15629"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="E7F354E1-8263-43BD-9D01-2AAAF1C6316F"
/>
# Recover deleted Resource Group
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Resource group recovery scoping question",
    "fileAttachmentHint": "",
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
            "required": true
        },
        {
            "id": "recover_all_accounts",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you want to recover all storage accounts in this resource group?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                }
            ],
            "required": true
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
    ]
}
---