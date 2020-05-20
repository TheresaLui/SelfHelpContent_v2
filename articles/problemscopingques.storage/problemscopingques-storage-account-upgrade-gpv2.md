<properties
	pageTitle="Upgrade to GPv2 storage account"
	description="Issue with upgrading to General Purpose V2 (GPv2) account"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32691091"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="B00DF825-A260-4F27-93A6-F269BDDF2204"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Upgrade to premium storage 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "formElements": [
        {
            "id": "upgrade_method",
            "order": 0,
            "controlType": "dropdown",
            "displayLabel": "Upgrade method",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "portal",
                    "text": "Portal"
                },
                {
                    "value": "powershell",
                    "text": "PowerShell"
                },
                {
                    "value": "cli",
                    "text": "Azure CLI"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message received",
            "required": false
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
