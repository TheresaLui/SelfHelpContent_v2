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
    "diagnosticCard": {
        "title": "Azure Files On premise AD DS Queries",
        "description": "The Azure Files troubleshooter can help resolve your queries related to on-premises AD DS authentication. Submit your query to determine the best possible solution",
        "insightNotAvailableText": "Our troubleshooter did not identify remediation for your issue. See the recommended documentation link to troubleshoot your issue"
    },
    "formElements": [
        {
            "id": "run_through_prereq",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you run the prerequisites in the feature enablement document?",
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
            "displayLabel": "Is the virtual machine you used to mount Azure Files using AD credentials domain joined to AD (also referred to as AD DS)?",
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
            "displayLabel": "Did you run the feature enablement steps, including creating an AD identity representing your storage account?",
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
            "displayLabel": "Have you granted share-level permission to the target user through RBAC?",
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
            "displayLabel": "Have you granted file/directory level permissions (NTFS ACLs) to the target user through file explorers or the icacls command?",
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
            "watermarkText": "How to enable on-premises AD DS Authentication for Azure Files",
            "displayLabel": "Enter your query",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
