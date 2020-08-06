<properties
         pageTitle="Scoping questions for MARS scheduled backup is not run automatically"
         description="Scoping questions for MARS scheduled backup is not run automatically"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632792"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
   	 articleId="c8ce31ba-6bd9-4d73-8109-8fb6dd37f86c"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions MARS scheduled backup is not run automatically
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "MARS scheduled backup is not run automatically",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "os_version",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the impacted system?",
            "watermarkText": "ex. Windows 2012 R2",
            "required": false
        },
        {
            "id": "machine_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the Windows Server or Windows Client",
            "required": true
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 3,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check <a href='https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
                },
                {
                    "value": "Ensure Windows Server backup schedule does not conflict with Azure files and folders backup schedule",
                    "text": "Ensure Windows Server backup schedule does not conflict with Azure files and folders backup schedule"
                },
                {
                    "value": "PowerShell 3.0 or later is installed on the server",
                    "text": "PowerShell 3.0 or later is installed on the server"
                },
                {
                    "value": "Ensure execution policy is set to Unrestricted or RemoteSigned",
                    "text": "Ensure execution policy is set to Unrestricted or RemoteSigned"
                },
                {
                    "value": "Ensure that Microsoft-OnlineBackup status is set to Enabled",
                    "text": "Ensure that Microsoft-OnlineBackup status is set to Enabled"
                },
                {
                    "value": "Ensure the user account selected for running the task is either SYSTEM or Local Administrators group on the server",
                    "text": "Ensure the user account selected for running the task is either SYSTEM or Local Administrators group on the server"
                },
                {
                    "value": "Ensure that ad-hoc backup is working",
                    "text": "Ensure that ad-hoc backup is working"
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
