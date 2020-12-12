<properties
	pageTitle="Troubleshooting migration issue"
	description="Troubleshooting migration issue"
	authors="kartikshah9"
	ms.author="kashah"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743033"
	productPesIds="16598"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest,usnat,ussec"
	schemaVersion="1"
	articleId="1b75d8aa-f9ae-470f-b115-101e0942bd10"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshooting migration issue
---
{
	"$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Troubleshooting migration issue",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Want to troubleshoot a data migration issue?",
        "description": "Our Azure Data Migration Troubleshooter can help you troubleshoot the data migration issue for your specific scenario. Please fill in the information below to find a solution.",
        "insightNotAvailableText": "Our troubleshooter did not find any issue for your migration. Please ensure the information provided is accurate and in the approved format. Also, see our manual steps below to find a solution."
    },
    "formElements": [
	{
		"id": "adlsgen2_migration_scenario",
		"order": 1,
		"controlType": "dropdown",
		"displayLabel": "Which scenario did you have issue with",
		"dropdownOptions": [
			{
				"value": "copy_large_files_from_localonpremise_to_adlsgen2",
				"text": "Upload files (over 100 GB) to Azure Data Lake Gen2 storage"
			},
			{
				"value": "copy_large_adlsgen2_files_to_localonpremise",
				"text": "Download files (over 100 GB)"
			},
			{
				"value": "copy_from_localonpremise_to_adlsgen2",
				"text": "Upload files (less than 100 GB) to Azure Data Lake Gen2 storage"
			},
			{
				"value": "copy_adlsgen2_to_localonpremise",
				"text": "Download files (less than 100 GB)"
			},
			{
				"value": "copy_adlsgen2_to_blobs",
				"text": "Copy Azure Data Lake Gen2 files to Azure Blob storage"
			},
			{
				"value": "copy_blobs_to_adlsgen2",
				"text": "Copy Azure Blobs to Azure Data Lake Gen2 storage"
			},
			{
				"value": "copy_adlsgen2_to_files",
				"text": "Copy Azure Data Lake Gen2 files to Azure Files storage"
			},
			{
				"value": "copy_files_to_adlsgen2",
				"text": "Copy Azure Files to Azure Data Lake Gen2 storage"
			},
			{
				"value": "copy_adlsgen2_to_adlsgen2",
				"text": "Copy Azure Data Lake Gen2 files to Azure Data Lake Gen2 storage"
			},
			{
				"value": "copy_from_aws_s3_to_adlsgen2",
				"text": "Copy files from AWS S3 to Azure Data Lake Gen2 storage"
			},
			{
				"value": "copy_from_otherexternalcloud_to_adlsgen2",
				"text": "Copy files from other external cloud (Google cloud, etc.) to Azure Data Lake Gen2 storage"
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
		"visibility": "adlsgen2_migration_scenario == copy_large_adlsgen2_files_to_localonpremise || adlsgen2_migration_scenario == copy_adlsgen2_to_localonpremise || adlsgen2_migration_scenario == copy_adlsgen2_to_blobs || adlsgen2_migration_scenario == copy_blobs_to_adlsgen2 || adlsgen2_migration_scenario == copy_adlsgen2_to_files || adlsgen2_migration_scenario == copy_files_to_adlsgen2 || adlsgen2_migration_scenario == copy_adlsgen2_to_adlsgen2",
		"order": 2,
		"controlType": "dropdown",
		"displayLabel": "Source storage account",
		"watermarkText": "Select the source storage account",
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
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
    },
	{
		"id": "storage_account_from_other",
		"visibility": "storage_account_from == dont_know_answer",
		"order": 3,
		"controlType": "textbox",
		"displayLabel": "Source storage account name",
		"watermarkText": "Enter storage account name",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "storage_account_to",
		"visibility": "adlsgen2_migration_scenario == copy_large_files_from_localonpremise_to_adlsgen2 || adlsgen2_migration_scenario == copy_from_localonpremise_to_adlsgen2 || adlsgen2_migration_scenario == copy_adlsgen2_to_blobs || adlsgen2_migration_scenario == copy_blobs_to_adlsgen2 || adlsgen2_migration_scenario == copy_adlsgen2_to_files || adlsgen2_migration_scenario == copy_files_to_adlsgen2 || adlsgen2_migration_scenario == copy_adlsgen2_to_adlsgen2 || adlsgen2_migration_scenario == copy_from_aws_s3_to_adlsgen2 || adlsgen2_migration_scenario == copy_from_otherexternalcloud_to_adlsgen2",
		"order": 4,
		"controlType": "dropdown",
		"displayLabel": "Destination storage account",
		"watermarkText": "Select target storage account",
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
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "storage_account_to_other",
		"visibility": "storage_account_to == dont_know_answer",
		"order": 5,
		"controlType": "textbox",
		"displayLabel": "Storage account name",
		"watermarkText": "Enter storage account name",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "IssueType",
		"order": 6,
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
				"text": "Connectivity (Timeout, Network Error, Cannot connect, Availability, etc)"
			},
			{
				"value": "MigrationTool",
				"text": "Issue with using migration tools (AzCopy, Storage resource explorer, Azure CLI, Azure Powershell, Rest Api, Azure File Sync, etc)"
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
		"visibility": "IssueType == Performance && (adlsgen2_migration_scenario == copy_large_files_from_localonpremise_to_adlsgen2 || adlsgen2_migration_scenario == copy_large_adlsgen2_files_to_localonpremise || adlsgen2_migration_scenario == copy_from_localonpremise_to_adlsgen2 || adlsgen2_migration_scenario == copy_adlsgen2_to_localonpremise)",
		"order": 7,
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
		"visibility": "IssueType == Performance && (adlsgen2_migration_scenario == copy_large_files_from_localonpremise_to_adlsgen2 || adlsgen2_migration_scenario == copy_large_adlsgen2_files_to_localonpremise || adlsgen2_migration_scenario == copy_from_localonpremise_to_adlsgen2 || adlsgen2_migration_scenario == copy_adlsgen2_to_localonpremise)",
		"order": 8,
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
		"id": "migration_tool",
		"visibility": "IssueType == Performance || IssueType == MigrationTool",
		"order": 9,
		"controlType": "dropdown",
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
				"value": "AzureFileSync",
				"text": "Azure File Sync"
			},
			{
				"value": "AzStorageRestApi",
				"text": "Azure Storage Rest Api"
			},
			{
				"value": "AzDataFactory",
				"text": "Azure Data Factory"
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
		"id": "azcopy_version",
		"visibility": "migration_tool == AzCopy",
		"order": 10,
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
		"id": "error_code_dropdown",
		"visibility": "IssueType != Performance && IssueType != MigrationTool",
		"order": 11,
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
		"visibility": "IssueType != Performance && IssueType != MigrationTool",
		"order": 12,
		"controlType": "textbox",
		"displayLabel": "Storage server Request ID",
		"watermarkText": "Request ID of failed operation ending with 000000",
		"textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
		"required": false,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "problem_start_time",
		"order": 13,
		"controlType": "datetimepicker",
		"displayLabel": "Approximate start time of the most recent occurrence",
		"required": true,
		"diagnosticInputRequiredClients": "Portal,ASC"
	},
	{
		"id": "problem_description",
		"order": 14,
		"controlType": "multilinetextbox",
		"displayLabel": "Details",
		"watermarkText": "Provide additional information about your issue",
		"required": true,
		"useAsAdditionalDetails": true,
		"hints": [{
				"text": "Issue description."
			}, {
				"text": "Provide additional information about your issue"
			}
		]
	}]
}
---