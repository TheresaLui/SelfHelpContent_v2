<properties
	pageTitle="How to choose data migration solution"
	description="How to choose data migration solution"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32631235,32632044"
	productPesIds="15629,16459"
	cloudEnvironments="public,MoonCake,FairFax"
	schemaVersion="1"
	articleId="E4579893-8E9C-469C-A21A-D84EEEFAD4A9"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# How to choose data migration solution
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "How to choose data migration solution",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "data_size",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Estimated data size to migrate",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "under50GB",
                    "text": "Under 50 GB"
                },
                {
                    "value": "50GB_100GB",
                    "text": "50 GB - 100 GB"
                },
                {
                    "value": "100GB_1TB",
                    "text": "100 GB - 1 TB"
                },
                {
                    "value": "1TB_50TB",
                    "text": "1 TB - 50 TB"
                },
                {
                    "value": "50TB_100TB",
                    "text": "50 TB - 100 TB"
                },
                {
                    "value": "100TB_500TB",
                    "text": "100 TB - 500 TB"
                },
                {
                    "value": "500TB_1PB",
                    "text": "500 TB - 1 PB"
                },
                {
                    "value": "1PB_5PB",
                    "text": "1 PB - 5 PB"
                },
                {
                    "value": "over5PB",
                    "text": "Greater than 5 PB"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
         {
            "id": "network_bandwidth",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Approximate available network bandwidth",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "under45Mbps",
                    "text": "Under 45 Mbps"
                },
                {
                    "value": "45Mbps_100Mbps",
                    "text": "45 Mbps - 100 Mbps"
                },
                {
                    "value": "100Mbps_500Mbps",
                    "text": "100 Mbps - 500 Mbps"
                },
                {
                    "value": "500Mbps_1Gbps",
                    "text": "500 Mbps - 1 Gbps"
                },
                {
                    "value": "1Gbps_5Gbps",
                    "text": "1 Gbps - 5 Gbps"
                },
                {
                    "value": "5Gbps_10Gbps",
                    "text": "5 Gbps - 10 Gbps"
                },
                {
                    "value": "10Gbps_40Gbps",
                    "text": "10 Gbps - 40 Gbps"
                },
                {
                    "value": "40Gbps_100Gbps",
                    "text": "40 Gbps - 100 Gbps"
                },
                {
                    "value": "over100Gbps",
                    "text": "Greater than 100 Gbps"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
        {
            "id": "error_code",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Transfer frequency",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "once",
                    "text": "Once"
                },
                {
                    "value": "many",
                    "text": "Repeatedly"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
