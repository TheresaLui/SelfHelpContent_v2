<properties
	pageTitle="Upgrade to premium storage"
	description="Issue with upgrading to premium storage"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32691092"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="E675A3B2-AE69-4ECE-9628-8B3E123D7DF3"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Upgrade to premium storage 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "formElements": [
        {
            "id": "premium_tier",
            "order": 0,
            "controlType": "dropdown",
            "displayLabel": "Premium storage type to upgrade to",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "premium_storage",
                    "text": "Premium Storage (Disks)"
                },
                {
                    "value": "premium_block_blobs",
                    "text": "Premium Block Blobs"
                },
                {
                    "value": "premium_files",
                    "text": "Premium Files"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
