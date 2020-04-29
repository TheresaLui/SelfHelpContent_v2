<properties
	pageTitle="Storage Blob Container recovery"
	description="Storage Blob Container recovery scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602730"
	productPesIds="16459"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="c5205999-f0e2-41c5-96d1-b711cd8498c2"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Recover deleted Blob Container
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Blob Container recovery scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "recovery_option",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Recovery Option",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "by_container_name",
                    "text": "Recover by container name"
                },
                {
                    "value": "by_time_period",
                    "text": "Recover by deleted time period"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "blob_container",
            "order": 2,
            "visibility": "recovery_option == by_container_name",
            "controlType": "textbox",
            "displayLabel": "Name of Container to recover",
            "watermarkText": "container1;container2;container3",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Local start time when container was deleted",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 5,
            "visibility": "recovery_option == by_time_period",
            "controlType": "datetimepicker",
            "displayLabel": "Local end time when container was deleted (cannot be same as Local start time)",
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
