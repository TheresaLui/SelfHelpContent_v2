<properties
         pageTitle="Scoping questions for MARS backup failure"
         description="Scoping questions for MARS backup failure"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553275"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="9e7d5d78-5ea7-4985-ac04-19ee33642d4d"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions MARS backup failure
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "MARS backup failure",
    "fileAttachmentHint": "Please upload all CBEngine log files located at C:\\\\Program Files\\\\Microsoft Azure Recovery Services Agent\\\\Temp. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
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
            "id": "backup_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this an initial/incremental backup failure?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Initial backup failure",
                    "text": "Initial backup failure"
                },
                {
                    "value": "Incremental backup failure",
                    "text": "Incremental backup failure"
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
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
            "watermarkText": "Copy and paste error message text from console",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 5,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check Microsoft Azure Recovery Services Agent <a href='https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#basic-troubleshooting'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
                },
                {
                    "value": "Firewall settings on the machine/proxy are configured to allow the required URLs",
                    "text": "Firewall settings on the machine/proxy are configured to allow the required URLs"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "5-10% free volume space is available on scratch folder location",
                    "text": "5-10% free volume space is available on scratch folder location"
                },
                {
                    "value": "A valid security PIN is entered",
                    "text": "A valid security PIN is entered"
                },
                {
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
                },
                {
                    "value": "Proxy is enabled",
                    "text": "Proxy is enabled"
                },
                {
                    "value": "Unsupported drives are excluded from backup",
                    "text": "Unsupported drives are excluded from backup"
                },
                {
                    "value": "Files with unsupported attributes are excluded from backup",
                    "text": "Files with unsupported attributes are excluded from backup"
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
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Please provide the ResourceId:",
            "infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 9,
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
