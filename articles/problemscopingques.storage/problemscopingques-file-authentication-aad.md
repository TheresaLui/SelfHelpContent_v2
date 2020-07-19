<properties
	pageTitle="Connecting to Azure Files using AAD DS Authentication"
	description="Connecting to Azure Files using AAD DS Authentication"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629551"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="E35FE4ED-E4F2-4615-8F38-6CFC8B15BBF1"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage Files Authentication using AAD DS
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Files Authentication - AAD DS",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "aad_ds_enabled",
            "order": 0,
            "controlType": "dropdown",
            "displayLabel": "Do you have AAD DS Authentication feature enabled on your storage account?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "ran_through_prereq",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you ran through the prerequisites in the feature enablement doc?",
            "watermarkText": "Choose an option",
            "visibility": "aad_ds_enabled == yes",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "aad_ds_vm",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the virtual machine you used to mount Azure Files using AAD credentials domain joined to AAD DS?",
            "watermarkText": "Choose an option",
            "visibility": "ran_through_prereq == yes",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "share_permission",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you granted share level permission to the target user through RBAC?",
            "watermarkText": "Choose an option",
            "visibility": "aad_ds_vm == yes",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "directory_permission",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you granted file/directory level permissions (NTFS ACLs) to the target user through file explorers or icacls?",
            "watermarkText": "Choose an option",
            "visibility": "share_permission == yes",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
