<properties 
  pageTitle="Azure Backup services"
  description="Azure Backup services"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740067"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="651aa678-afe2-44fe-a049-72674ab693dd"
  ownershipId="AzureData_AzureSQLVM"
/>
# Azure Backup services
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Backup services",
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
            "id": "what_method",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What operation are you performing?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Backup my databases",
                    "value": "BackupDatabase"
                },
                {
                    "text": "Restore my databases",
                    "value": "RestoreDatabase"
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
            "id": "which_feature",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the feature you are using to backup/restore from?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "SQL Server Database backup on Azure VM",
                    "value": "SQLServerDatabasebackuponAzure VM"
                },
                {
                    "text": "Azure VM Backup",
                    "value": "AzureVMBackup"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
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
