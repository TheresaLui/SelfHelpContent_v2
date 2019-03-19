<properties pageTitle="SQL Server Backup Restore"
	 description="SQL Server Backup Restore"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633516"
	 productPesIds="14745"
	 cloudEnvironments="public"
	 schemaVersion="1"
	 articleId="bc1ede95-f07e-43dd-a757-a3162188068c"
/>
# SQL Server Backup Restore
---
{
    "resourceRequired": false,
    "title": "SQL Server Backup Restore",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whichPhase",
            "visibility": null,
            "order": 1,
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
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whichService",
            "visibility": null,
            "order": 2,
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
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whatMethod",
            "visibility": "whichPhase != Planning",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What method are you using/planning to use for the backup or restore operation?",
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
                    "text": "T-SQL Backup or Restore command",
                    "value": "TSQL"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
       {
            "id": "whereWritten",
            "visibility": "whichPhase != Planning && whichService == Backup",
            "order": 4,
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
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        }
    ]
}
---
