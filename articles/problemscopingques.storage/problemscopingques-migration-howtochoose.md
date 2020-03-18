<properties
	pageTitle="How to choose data migration solution"
	description="How to choose data migration solution"
	authors="Sijia"
    	ms.author="siz"
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
            "id": "source_resource",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Source resource",
            "watermarkText": "Select source resource to migrate from",
            "dropdownOptions": [
                {
                    "value": "storage_accout",
                    "text": "Azure Storage Account"
                },
                {
                    "value": "blob",
                    "text": "Azure Blob"
                },
                {
                    "value": "files",
                    "text": "Azure Files"
                },
                {
                    "value": "adlsgen2",
                    "text": "Azure Data Lake Storage Gen2"
                },
                {
                    "value": "managed_disks",
                    "text": "Azure Disks (managed)"
                },
                {
                    "value": "local/on_premise",
                    "text": "Local/On-Premise"
                },
                {
                    "value": "external_clouds",
                    "text": "External Clouds (Amazon S3, GCP, etc)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
	{
            "id": "destination_resource",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Destination resource",
            "watermarkText": "Select destination resource to migrate to",
            "dropdownOptions": [
                {
                    "value": "storage_accout",
                    "text": "Azure Storage Account"
                },
                {
                    "value": "blob",
                    "text": "Azure Blob"
                },
                {
                    "value": "files",
                    "text": "Azure Files"
                },
                {
                    "value": "adlsgen2",
                    "text": "Azure Data Lake Storage Gen2"
                },
                {
                    "value": "managed_disks",
                    "text": "Azure Disks (managed)"
                },
                {
                    "value": "local/on_premise",
                    "text": "Local/On-Premise"
                },
                {
                    "value": "external_clouds",
                    "text": "External Clouds (Amazon S3, GCP, etc)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true
        },
        {
            "id": "data_size_tb",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Estimated data size to migrate",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "0.05",
                    "text": "50 GB"
                },
                {
                    "value": "0.1",
                    "text": "100 GB"
                },
                {
                    "value": "1",
                    "text": "1 TB"
                },
                {
                    "value": "50",
                    "text": "50 TB"
                },
                {
                    "value": "100",
                    "text": "100 TB"
                },
                {
                    "value": "500",
                    "text": "500 TB"
                },
                {
                    "value": "1000",
                    "text": "1 PB"
                },
                {
                    "value": "5000",
                    "text": "5 PB"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": false
        },
         {
            "id": "network_bandwidth",
            "order": 4,
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
            "required": false
        },
        {
            "id": "transfer_frequency",
            "order": 5,
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
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
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
