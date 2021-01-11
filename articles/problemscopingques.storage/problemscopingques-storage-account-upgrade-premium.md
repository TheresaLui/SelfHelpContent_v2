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
    "resourceRequired": false,
    "title": "Issue with storage account premium tier",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to troubleshoot an issue with premium tier?",
        "description": "Please fill in the information below to find a solution.",
        "insightNotAvailableText": "Our troubleshooter did not find any issue. Please ensure the information provided is accurate and in the approved format. Also, see our manual steps below to find a solution."
    },
    "formElements": [
        {
            "id": "premium_tier",
            "order": 0,
            "controlType": "dropdown",
            "displayLabel": "Upgrade to this premium storage type",
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
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "acct_premium_tier_failure_scenario",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which scenario did you have an issue with",
            "dropdownOptions": [
                {
                    "value": "cannot_create_premium_v1_or_v2_acct_for_zone_or_geo_repl",
                    "text": "Cannot create premium StorageV2 (general purpose v2) account or premium Storage (general purpose v1) account with zone or geo replication type (GRS/RA-GRS/ZRS/GZRS/RA-GZRS)"
                },
                {
                    "value": "cannot_create_premium_blockblob_or_file_acct_for_zrs",
                    "text": "Cannot create premium BlockBlobStorage or FileStorage account with zone replication type (ZRS/GZRS/RA-GZRS)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
