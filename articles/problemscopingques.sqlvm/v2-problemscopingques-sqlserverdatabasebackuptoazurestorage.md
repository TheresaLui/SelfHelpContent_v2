<properties 
  pageTitle="SQL Server database backup to Azure Storage"
  description="SQL Server database backup to Azure Storage"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740094"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="704bfbc7-90e8-4b25-ad1b-cd0906418c05"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server database backup to Azure Storage (Backup to URL)
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Server database backup to Azure Storage",
    "fileAttachmentHint": null,
    "diagnosticCard": {
    "title": "Backup to Azure Storage Troubleshooter",
    "description": "Our Backup to Azure Storage Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "what_phase",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What phase of implementation are you at?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I'm still planning/have general questions",
                    "value": "Planning"
                },
                {
                    "text": "I'm setting it up and need help",
                    "value": "SettingBackupRestoreHelp"
                },
                {
                    "text": "I've got a backup/restore that is failing",
                    "value": "FailedBackupRestore"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "which_service",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you need assistance with backup or restore?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Backup",
                    "value": "Backup"
                },
                {
                    "text": "Restore",
                    "value": "Restore"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "what_method",
            "visibility": "what_phase != null && what_phase != Planning",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What method are you using for the backup or restore operation?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "SQL Agent Jobs",
                    "value": "SQLAgentJobs"
                },
                {
                    "text": "SQL Maintenance plan",
                    "value": "SQLMaintenancePlan"
                },
                {
                    "text": "T-SQL Backup or Restore command",
                    "value": "TSQL"
                },
                {
                    "text": "I'm not sure/don't know",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whereWritten",
            "visibility": "what_phase != null && what_phase != Planning && which_service == Backup",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where are the backups being written?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure Storage Account",
                    "value": "BackupToStorageAccount"
                },
                {
                   "text": "Azure File Share",
                   "value": "AzureFileShare"
                },
                {
                    "text": "I'm not sure/don't know",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "error_message_backup",
            "visibility": "what_phase == FailedBackupRestore",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Which error message are you receiving?",
            "watermarkText": "Provide the error message",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "backuptoazurestorage_issue_type",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes your Backup to Azure Storage issue.",
            "watermarkText": "Common Backup to Azure Storage issue categories",
            "infoBalloonText": "Backup to Azure Storage issue category",
            "dropdownOptions": [
            {
            "value": "DatabaseBackupFailure_BlockSizeReached_Error_3063",
            "text": "3063: Write to backup block blob device failed"
            },
            {
            "value": "MigrateDatabaseToAzureVM",
            "text": "Migrate Databases from On Premise/Another Cloud to Azure VM"
            },
            {
            "value": "DatabaseBackupFailure_OSError50_Error_3201",
            "text": "3201: Cannot open backup device"
            },
            {
            "value": "DatabaseBackupFailure_DifferentialBackup_AzureBackUpService_Error_3035",
            "text": "3035: Cannot perform a differential backup for database"
            },
            {
            "value": "DatabaseBackupFailure_1TB_PageBlob_Error_416",
            "text": "416: Cannot backup database of 1 TB or more to Page blob"
            },
            {
            "value": "DatabaseBackupFailure_TLS_Error_3271",
            "text": "3271: Backup fails due to TLS errors"
            },
            {
            "value": "DatabaseBackupFailure_1TB_ActiveLease_Error_412",
            "text": "412: Backup Files with active lease and show as 1 TB Size on storage account"
            },
            {
            "value": "DatabaseBackupFailure_ProxyServer",
            "text": "Backup failed due to proxy server issues"
            },
            {
            "value": "DatabaseBackupFailure_LongRunning",
            "text": "My backup is taking longer to complete/ Database Restore is slow"
            },
            {
            "value": "DatabaseRestoreFailure_RestoringFromStorageAccount_Error_3284",
            "text": "3284: Restore database from storage account fails"
            },
            {
            "value": "dont_know_answer",
            "text": "None of the above"
            }
        ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
    },
    {
        "id": "backuptoazurestorage_proxyserver_issue_type",
        "order": 2100,
        "controlType": "dropdown",
        "displayLabel": "Choose an option that best describes your proxy server issue Types.",
        "watermarkText": "Proxy Server Issue Types",
        "infoBalloonText": "Proxy Server Issue Types",
        "dropdownOptions": [
            {
            "value": "NonrecoverableIOErrorBackupDatabase_Error_3013",
            "text": "3013: A nonrecoverable I/O error occurred on file Backup Database Terminating abnormally"
            },
            {
            "value": "MigrateDatabaseToAzureVM",
            "text": "Migrate Databases from On Premise/Another Cloud to Azure VM"
            },
            {
            "value": "BackupToURL_Error",
            "text": "Backup to URL received an exception from the remote endpoint"
            },
            {
            "value": "BackupIORequest_Error",
            "text": "BackupIORequest::ReportIoError: write failure on backup device"
            },
            {
            "value": "NonrecoverableIOErrorProxy_Error_407",
            "text": "407: A nonrecoverable I/O error occurred on file : Proxy Authentication Required"
            },
            {
            "value": "dont_know_answer",
            "text": "None of the above"
            }
        ],
        "required": false,
        "diagnosticInputRequiredClients": "Portal",
        "visibility": "backuptoazurestorage_issue_type == DatabaseBackupFailure_ProxyServer"
    }
    ],
    "$schema": "SelfHelpContent"
}
---
