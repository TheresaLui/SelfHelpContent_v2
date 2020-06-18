<properties 
  pageTitle="Automated or Managed backup"
  description="Automated or Managed backup"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740066"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="1ddddd16-01e5-4b9d-8458-f8d4d38f06ac"
 ownershipId="AzureData_AzureSQLVM"
/>
# Automated or Managed backup 
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Automated or Managed backup",
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
                    "text": "Automated Backup(From SQL Resource Provider)",
                    "value": "AutomatedBackup"
                },
                {
                    "text": "Managed Backup",
                    "value": "ManagedBackup"
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
