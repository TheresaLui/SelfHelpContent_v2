<properties
	pageTitle="Troubleshooting migration issue"
	description="Troubleshooting migration issue"
	authors="Sijia"
	ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743317,32743316,32743318,32743033"
	productPesIds="15629,16459,16460,16598"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="65bbc16c-94c9-4449-9852-31c676302f4d"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshooting migration issue
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Troubleshooting migration issue",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to troubleshoot a data migration issue?",
        "description": "Our Azure Data Migration Troubleshooter can help you troubleshoot the data migration issue for your specific scenario. Please fill in the information below to find a solution.",
        "insightNotAvailableText": "Our troubleshooter did not find any issue for your migration. Please ensure the information provided is accurate and in the approved format. Also, see our manual steps below to find a solution."
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
		"id": "storage_account_from",
		"visibility": "source_resource == storage_account || source_resource == blob || source_resource == files || source_resource == adlsgen2",
		"order": 9,
		"controlType": "dropdown",
		"displayLabel": "Source storage account",
		"watermarkText": "Select storage account to migrate from",
		"infoBalloonText": "Select source storage account for the failed operation/request, it can be same as the one from previous Basic tab",
		"dynamicDropdownOptions": {
			"uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
			"jTokenPath": "value",
			"textProperty": "id",
			"valueProperty": "id",
			"textPropertyRegex": "[^/]+$",
			"defaultDropdownOptions": {
				"value": "dont_know_answer",
				"text": "From a different subscription, external source or not applicable"
			}
		},
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
    },
	{
		"id": "storage_account_from_other",
		"visibility": "storage_account_from == dont_know_answer",
		"order": 10,
		"controlType": "textbox",
		"displayLabel": "Source storage account name",
		"watermarkText": "Enter storage account name",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "storage_account_to",
		"order": 11,
		"controlType": "dropdown",
		"displayLabel": "Destination storage account",
		"watermarkText": "Select storage account to migrate to",
		"infoBalloonText": "Select not applicable for (a) Blob/File download; (b) Account upgrade/migration; (c) Disk operations not involving a storage account",
		"dynamicDropdownOptions": {
			"uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
			"jTokenPath": "value",
			"textProperty": "id",
			"valueProperty": "id",
			"textPropertyRegex": "[^/]+$",
			"defaultDropdownOptions": {
				"value": "dont_know_answer",
				"text": "From a different subscription, external source or not applicable"
			}
		},
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "storage_account_to_other",
		"visibility": "storage_account_to == dont_know_answer",
		"order": 12,
		"controlType": "textbox",
		"displayLabel": "Destination storage account name",
		"infoBalloonText": "Specify destination acount name if applicable (e.g. if it's from another subscription); If you are moving a storage account to a new subscription, specify the destination subscription Id here",
		"watermarkText": "Enter storage account name or subscription id if applicable",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "IssueType",
		"order": 13,
		"controlType": "dropdown",
		"displayLabel": "Issue type",
		"watermarkText": "Choose an option",
		"dropdownOptions": [
			{
				"value": "Performance",
				"text": "Performance (Slow transfer, High latency, Throttling, Hang, Stuck, etc)"
			},
			{
				"value": "Permission",
				"text": "Authentication, Authorization (Firewall/Virtual networks, SAS/Shared key, AAD/RBAC, etc)"
			},
			{
				"value": "Connectivity",
				"text": "Connectivity (Timeout, Cannot connect, Availability, etc)"
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
		"id": "migration_tool",
		"order": 14,
		"controlType": "dropdown",
		"infoBalloonText": "Choose the tool used for migration which had the issue",
		"displayLabel": "Migration tool",
		"watermarkText": "Choose an option",
		"dropdownOptions": [
			{
				"value": "AzCopy",
				"text": "AzCopy"
			},
			{
				"value": "AzStorageExplorer",
				"text": "Azure Storage Explorer"
			},
			{
				"value": "AzPortal",
				"text": "Azure Portal"
			},
			{
				"value": "AzPowershell",
				"text": "Azure Powershell"
			},
			{
				"value": "AzCli",
				"text": "Azure CLI"
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
		"id": "azcopy_version",
		"visibility": "migration_tool == AzCopy",
		"order": 15,
		"controlType": "dropdown",
		"displayLabel": "AzCopy version",
		"watermarkText": "Choose an option",
		"dropdownOptions": [
			{
				"value": "AzCopy_above10.1",
				"text": "v10.1.0 and above"
			},
			{
				"value": "AzCopy_10_10.0.9",
				"text": "v10.0.0 - 10.0.9"
			},
			{
				"value": "AzCopy_below8.1",
				"text": "v8.1 and below"
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
		"id": "other_migration_tool_version",
		"visibility": "migration_tool != AzCopy && migration_tool != AzPortal && migration_tool != dont_know_answer",
		"order": 16,
		"controlType": "textbox",
		"infoBalloonText": "Specify the digital verion of the tool used for migration which had the issue",
		"displayLabel": "Migration tool version",
		"watermarkText": "Tool version if applicable in format of X.X.X",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "azcopy_command_needhelp",
		"visibility": "migration_tool == AzCopy",
		"order": 17,
		"controlType": "dropdown",
		"infoBalloonText": "Choose yes if you need any help on correct syntax of azcopy command",
		"displayLabel": "Do you have questions on AzCopy command",
		"watermarkText": "Choose an option",
		"dropdownOptions": [
			{
				"value": "yes",
				"text": "yes"
			},
			{
				"value": "no",
				"text": "no"
			},
			{
				"value": "dont_know_answer",
				"text": "Don't know"
			}
		],
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "error_code_dropdown",
		"order": 18,
		"controlType": "dropdown",
		"displayLabel": "Error code",
		"watermarkText": "HTTP error code of failed operation",
		"dropdownOptions": [
			{
				"value": "304",
				"text": "HTTP 304"
			},
			{
				"value": "400",
				"text": "HTTP 400"
			},
			{
				"value": "403",
				"text": "HTTP 403"
			},
			{
				"value": "404",
				"text": "HTTP 404"
			},
			{
				"value": "405",
				"text": "HTTP 405"
			},
			{
				"value": "409",
				"text": "HTTP 409"
			},
			{
				"value": "411",
				"text": "HTTP 411"
			},
			{
				"value": "412",
				"text": "HTTP 412"
			},
			{
				"value": "413",
				"text": "HTTP 413"
			},
			{
				"value": "415",
				"text": "HTTP 415"
			},
			{
				"value": "416",
				"text": "HTTP 416"
			},
			{
				"value": "500",
				"text": "HTTP 500"
			},
			{
				"value": "501",
				"text": "HTTP 501"
			},
			{
				"value": "502",
				"text": "HTTP 502"
			},
			{
				"value": "503",
				"text": "HTTP 503"
			},
			{
				"value": "other",
				"text": "Not listed above"
			}
		],
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "request_id",
		"order": 19,
		"controlType": "textbox",
		"displayLabel": "Storage server Request ID",
		"watermarkText": "Request ID of failed operation ending with 000000",
		"textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "problem_start_time",
		"order": 20,
		"controlType": "datetimepicker",
		"displayLabel": "Approximate start time of the most recent occurrence",
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "problem_description",
		"order": 21,
		"controlType": "multilinetextbox",
		"displayLabel": "Provide any additional details",
		"required": true,
		"useAsAdditionalDetails": true
	}
],
"$schema": "SelfHelpContent"
}
---
