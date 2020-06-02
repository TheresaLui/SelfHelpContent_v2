<properties
         pageTitle="Scoping questions for offline backup or seeding issues"
         description="Scoping questions for offline backup or seeding issues"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632796"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
    	 articleId="15e2bd99-2406-4639-b757-f8517ff0383d"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for offline backup or seeding issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "offline backup or seeding issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "backup_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "At what stage of offline seeding backup are you facing the issue?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Initiating offline backup",
                    "text": "Initiating offline backup"
                },
                {
                    "value": "Preparing SATA drives",
                    "text": "Preparing SATA drives"
                },
                {
                    "value": "Shipping SATA drives to Azure",
                    "text": "Shipping SATA drives to Azure"
                },
                {
                    "value": "Updating shipping details on the Azure Import job",
                    "text": "Updating shipping details on the Azure Import job"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text from failed job details dialog in Microsoft Azure Backup agent",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 3,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "<a href='https://docs.microsoft.com/azure/backup/backup-azure-backup-import-export#prerequisites'>Prerequisites</a> for offline backup",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
                },
                {
                    "value": "Ensure Azure PowerShell version 3.7.0 is installed on source and copy computer",
                    "text": "Ensure Azure PowerShell version 3.7.0 is installed on source and copy computer"
                },
                {
                    "value": "Microsoft Edge or Internet Explorer 11 is installed, and JavaScript is enabled",
                    "text": "Microsoft Edge or Internet Explorer 11 is installed, and JavaScript is enabled"
                },
                {
                    "value": "Azure Storage account and Recovery Services vault is in the same subscription",
                    "text": "Azure Storage account and Recovery Services vault is in the same subscription"
                },
                {
                    "value": "Azure login account has owner permission to perform offline backup",
                    "text": "Azure login account has owner permission to perform offline backup"
                },
                {
                    "value": "Ensure Microsoft.ImportExport is registered with the same subscription as Azure Storage account",
                    "text": "Ensure Microsoft.ImportExport is registered with the same subscription as Azure Storage account"
                },
                {
                    "value": "Ensure the staging location has enough free space to hold initial backup copy",
                    "text": "Ensure the staging location has enough free space to hold initial backup copy"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "get_machineid",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId:",
            "infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
