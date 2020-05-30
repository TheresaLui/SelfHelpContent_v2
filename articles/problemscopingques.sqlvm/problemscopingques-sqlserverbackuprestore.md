<properties pageTitle="SQL Server Backup Restore"
	 description="SQL Server Backup Restore"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633516"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax, usnat, ussec"
	 schemaVersion="1"
	 articleId="bc1ede95-f07e-43dd-a757-a3162188068c"
	ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server Backup Restore
---
{
    "resourceRequired": false,
    "title": "SQL Server Backup Restore",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
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
                    "text": "I’m still planning/have general questions",
                    "value": "Planning"
                },
                {
                    "text": "I’m setting it up and need help",
                    "value": "SettingBackupRestoreHelp"
                },
                {
                    "text": "I’ve got a backup/restore that is failing",
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
                    "text": "Automated Backup (SQL Configuration Blade)",
                    "value": "sqlIaasExtensionBlade"
                },
                {
                    "text": "SQL Managed Backup",
                    "value": "SQLManagedBackup"
                },
                {
                    "text": "SQL Maintenance plan",
                    "value": "SQLMaintenancePlan"
                },
                {
                    "text": "Azure Recovery Services",
                    "value": "AzureRecoveryServices"
                },
                {
                    "text": "T-SQL Backup or Restore command",
                    "value": "TSQL"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "dont_know_answer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
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
                    "text": "Local Disk",
                    "value": "LocalDisk"
                },
                {
                    "text": "Azure Storage (backup to URL)",
                    "value": "BackupToURL"
                },
                {
                    "text": "Azure Storage (file snapshot backup)",
                    "value": "FileSnapshotBackup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
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
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
