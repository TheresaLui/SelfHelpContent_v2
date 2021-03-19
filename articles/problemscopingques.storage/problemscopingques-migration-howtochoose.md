<properties
	pageTitle="How to choose data migration solution"
	description="How to choose data migration solution"
	authors="Sijia"
	ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32631235,32632044,32632043,32743032"
	productPesIds="15629,16459,16460,16598"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="E4579893-8E9C-469C-A21A-D84EEEFAD4A9"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# How to choose data migration solution
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "How to choose data migration solution",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to find a data migration solution?",
        "description": "Our Azure Data Migration Solution Finder can help you find the data migration solution for your specific scenario. Please fill in the information below to find a solution.",
        "insightNotAvailableText": "Our solution finder did not find any solution for your migration. Please ensure the information provided is accurate and in the approved format. Also, see our manual steps below to find a method."
    },
    "formElements": [
    	{
            "id": "source_resource",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Source resource",
            "watermarkText": "Select source resource to migrate from",
            "dropdownOptions": [
	    	{
	    		"value": "storage_account",
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
			"text": "Azure Disks"
		},
		{
			"value": "local_onpremise",
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
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "account_migration_scenario",
		"visibility": "source_resource == storage_account",
		"order": 2,
		"controlType": "dropdown",
		"displayLabel": "Migration Scenario",
		"watermarkText": "Select the applicable migration scenario",
		"dropdownOptions": [
		{
			"value": "move_account_to_new_subId",
			"text": "Move storage account to another subscription"
		},
		{
			"value": "move_account_to_new_rg",
			"text": "Move storage account to another resource group"
		},
		{
			"value": "move_account_to_new_region",
			"text": "Move storage account to another region"
		},
		{
			"value": "migrate_classic_account_to_arm",
			"text": "Migrate classic storage account to ARM"
		},
		{
			"value": "upgrade_gpv1_account_to_gpv2",
			"text": "Upgrade GPV1 storage account to GPV2"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know or not listed above"
		}
	],
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "blob_migration_scenario",
		"visibility": "source_resource == blob",
		"order": 3,
		"controlType": "dropdown",
		"displayLabel": "Migration Scenario",
		"watermarkText": "Select the applicable migration scenario",
		"dropdownOptions": [
		{
			"value": "copy_blobs_to_blobs",
			"text": "Copy Azure Blobs to Azure Blobs"
		},
		{
			"value": "copy_blobs_to_files",
			"text": "Copy Azure Blobs to Azure Files"
		},
		{
			"value": "copy_blobs_to_adlsgen2",
			"text": "Copy Azure Blobs to Azure Data Lake Gen2 storage"
		},
		{
			"value": "copy_blobs_to_managed_disk",
			"text": "Copy Azure Blobs to Managed Disk"
		},
		{
			"value": "copy_blobs_to_localonpremise",
			"text": "Download Azure Blobs to Local/On-Premise"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know or not listed above"
		}
	],
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "files_migration_scenario",
		"visibility": "source_resource == files",
		"order": 4,
		"controlType": "dropdown",
		"displayLabel": "Migration Scenario",
		"watermarkText": "Select the applicable migration scenario",
		"dropdownOptions": [
		{
			"value": "copy_files_to_blobs",
			"text": "Copy Azure Files to Azure Blobs"
		},
		{
			"value": "copy_files_to_files",
			"text": "Copy Azure Files to Azure Files"
		},
		{
			"value": "copy_files_to_adlsgen2",
			"text": "Copy Azure Files to Azure Data Lake Gen2 storage"
		},
		{
			"value": "copy_files_to_managed_disk",
			"text": "Copy Azure Files to Managed Disk"
		},
		{
			"value": "copy_files_to_localonpremise",
			"text": "Download Azure Files to Local/On-Premise"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know or not listed above"
		}
	],
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "adlsgen2_migration_scenario",
		"visibility": "source_resource == adlsgen2",
		"order": 5,
		"controlType": "dropdown",
		"displayLabel": "Migration Scenario",
		"watermarkText": "Select the applicable migration scenario",
		"dropdownOptions": [
		{
			"value": "copy_adlsgen2_to_blobs",
			"text": "Copy Azure Data Lake Gen2 files to Azure Blobs"
		},
		{
			"value": "copy_adlsgen2_to_files",
			"text": "Copy Azure Data Lake Gen2 files to Azure Files"
		},
		{
			"value": "copy_adlsgen2_to_adlsgen2",
			"text": "Copy Azure Data Lake Gen2 files to Azure Data Lake Gen2 storage"
		},
		{
			"value": "copy_adlsgen2_to_managed_disk",
			"text": "Copy Azure Data Lake Gen2 files to Managed Disk"
		},
		{
			"value": "copy_adlsgen2_to_localonpremise",
			"text": "Download Azure Data Lake Gen2 files to Local/On-Premise"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know or not listed above"
		}
	],
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "manageddisk_migration_scenario",
		"visibility": "source_resource == managed_disks",
		"order": 6,
		"controlType": "dropdown",
		"displayLabel": "Migration Scenario",
		"watermarkText": "Select the applicable migration scenario",
		"dropdownOptions": [
		{
			"value": "copy_vhd_to_blobs",
			"text": "Export/Copy the VHD of a managed disk to a storage account"
		},
		{
			"value": "copy_snapshot_to_blobs",
			"text": "Export/Copy managed snapshots as VHD to a storage account"
		},
		{
			"value": "copy_snapshot_to_subscription",
			"text": "Copy snapshot of managed disk to a subscription"
		},
		{
			"value": "copy_disk_to_subscription",
			"text": "Copy managed disk to same or different subscription within the same region"
		},
		{
			"value": "copy_vhd_to_region",
			"text": "Export/Copy the VHD of a managed disk to a region"
		},
		{
			"value": "copy_snapshot_to_region",
			"text": "Export/Copy managed snapshots as VHD to a region"
		},
		{
			"value": "copy_disk_to_region",
			"text": "Export/Copy managed disk to a region"
		},
		{
			"value": "migrate_premium_snapshot_to_standard",
			"text": "Migrate a snapshot from Premium storage to Standard"
		},
		{
			"value": "update_disk_storage_type",
			"text": "Change the storage type of a managed disk"
		},
		{
			"value": "migrate_lrs_snapshot_to_zrs",
			"text": "Migrate a snapshot from LRS to ZRS"
		},
		{
			"value": "convert_unmanaged_disk_to_managed",
			"text": "Convert a Windows virtual machine from unmanaged disks to managed disks"
		},
		{
			"value": "copy_vhd_to_localonpremise",
			"text": "Download the underlying VHD of a managed disk to Local/On-Premise"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know or not listed above"
		}
	],
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "local_onpremise_migration_scenario",
		"visibility": "source_resource == local_onpremise",
		"order": 7,
		"controlType": "dropdown",
		"displayLabel": "Migration Scenario",
		"watermarkText": "Select the applicable migration scenario",
		"dropdownOptions": [
		{
			"value": "copy_from_localonpremise_to_blobs",
			"text": "Upload Local/On-Premise files to Azure Blobs"
		},
		{
			"value": "copy_from_localonpremise_to_files",
			"text": "Upload Local/On-Premise files to Azure Files"
		},
		{
			"value": "copy_from_localonpremise_to_adlsgen2",
			"text": "Upload Local/On-Premise files to Azure Data Lake Gen2 Storage"
		},
		{
			"value": "copy_from_localonpremise_to_disk",
			"text": "Upload a vhd from Local/On-Premise to Azure managed disk"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know or not listed above"
		}
	],
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "external_cloud_migration_scenario",
		"visibility": "source_resource == external_clouds",
		"order": 8,
		"controlType": "dropdown",
		"displayLabel": "Migration Scenario",
		"watermarkText": "Select the applicable migration scenario",
		"dropdownOptions": [
		{
			"value": "copy_from_aws_s3_to_blobs",
			"text": "Copy files from Amazon S3 to Azure Blobs"
		},
		{
			"value": "copy_from_aws_s3_to_adlsgen2",
			"text": "Copy files from Amazon S3 to Azure Data Lake Gen2 Storage"
		},
		{
			"value": "copy_from_otherexternalcloud_to_blobs",
			"text": "Copy files from other external clouds to Azure Blobs"
		},
		{
			"value": "copy_from_otherexternalcloud_to_adlsgen2",
			"text": "Copy files from other external clouds to Azure Data Lake Gen2 Storage"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know or not listed above"
		}
	],
	"required": true,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "data_size_tb",
		"visibility": "source_resource != storage_account",
		"order": 9,
		"controlType": "dropdown",
		"displayLabel": "Estimated data size to migrate",
		"watermarkText": "Choose a data size",
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
	"required": false,
        "diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "network_bandwidth_mbps",
		"visibility": "source_resource != storage_account",
		"order": 10,
		"controlType": "dropdown",
		"displayLabel": "Approximate available network bandwidth",
		"watermarkText": "If you don't know network bandwidth, use this link to check: https://www.azurespeed.com/",
		"dropdownOptions": [
		{
			"value": "0",
			"text": "None"
		},
		{
			"value": "45",
			"text": "45 Mbps"
		},
		{
			"value": "100",
			"text": "100 Mbps"
		},
		{
			"value": "500",
			"text": "500 Mbps"
		},
		{
			"value": "1000",
			"text": "1 Gbps"
		},
		{
			"value": "5000",
			"text": "5 Gbps"
		},
		{
			"value": "10000",
			"text": "10 Gbps"
		},
		{
			"value": "40000",
			"text": "40 Gbps"
		},
		{
			"value": "100000",
			"text": "100 Gbps"
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
		"id": "transfer_frequency",
		"visibility": "source_resource != storage_account",
		"order": 11,
		"controlType": "dropdown",
		"displayLabel": "Transfer frequency",
		"watermarkText": "Choose an option",
		"dropdownOptions": [
		{
			"value": "once",
			"text": "Once"
		},
		{
			"value": "repeatedly",
			"text": "Repeatedly"
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
		"id": "problem_start_time",
		"order": 12,
		"controlType": "datetimepicker",
		"displayLabel": "Approximate start time of the most recent occurrence",
		"required": true
	},
	{
		"id": "problem_description",
		"order": 13,
		"controlType": "multilinetextbox",
		"displayLabel": "Provide any additional details",
		"required": true,
		"useAsAdditionalDetails": true
	}
],
"$schema": "SelfHelpContent"
}
---
