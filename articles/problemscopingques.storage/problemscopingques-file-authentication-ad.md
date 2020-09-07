<properties
	pageTitle="Connecting to Azure Files using AD Authentication"
	description="Connecting to Azure Files using AD Authentication"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32689882"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="fff900f7-0de9-46f3-aed0-ad0f880e496c"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage Files Authentication using AD
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Files Authentication - AD",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "ran_through_prereq",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you ran through the prerequisites in the feature enablement doc?",
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
            "id": "ad_vm",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the virtual machine you used to mount Azure Files using AD credentials domain joined to AD (also referred as AD DS)?",
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
            "id": "ad_enabled",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you ran the feature enablement steps including creating an AD identity representing your storage account?",
            "watermarkText": "Choose an option",
            "visibility": "ad_vm == yes",
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
            "id": "synced_ad_connect",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you synced your AD to Azure AD using Azure AD Connect?",
            "watermarkText": "Choose an option",
            "visibility": "ad_enabled == yes",
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
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you granted share level permission to the target user through RBAC?",
            "watermarkText": "Choose an option",
            "visibility": "synced_ad_connect == yes",
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
            "order": 6,
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
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
