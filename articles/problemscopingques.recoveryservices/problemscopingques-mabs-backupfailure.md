<properties
         pageTitle="Scoping questions for Azure backup server Online backup is failing"
         description="Scoping questions for Azure backup server Online backup is failing"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553284"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
  	 articleId="5784ce89-9b9c-4881-9caa-2a462fcbdc24"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure backup server - Online backup is failing
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure backup server Online backup is failing",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure backup server Online backup is failing",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "issue_Type",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the backup failure type:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Cloud backup is failing",
                    "text": "Cloud backup is failing"
                },
                {
                    "value": "Disk backup is failing",
                    "text": "Disk backup is failing"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "os_version",
            "order": 2,
            "visibility": "issue_Type == Cloud backup is failing || issue_Type == Disk backup is failing",
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the impacted Server?",
            "watermarkText": "ex. Windows 2012 R2",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "machine_name",
            "order": 3,
            "visibility": "issue_Type == Cloud backup is failing || issue_Type == Disk backup is failing",
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the impacted machine",
            "required": false
        },
        {
            "id": "mab_version",
            "order": 4,
            "visibility": "issue_Type == Cloud backup is failing || issue_Type == Disk backup is failing",
            "controlType": "textbox",
            "infoBalloonText": "You can find version information from Microsoft Azure Backup Server Console\\Help\\About",
            "displayLabel": "What is the software version of Microsoft Azure Backup Server?",
            "watermarkText": "ex. version 12.0.332.0.",
            "required": false
        },
        {
            "id": "backup_type",
            "order": 5,
            "visibility": "issue_Type == Cloud backup is failing",
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
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "error_message",
            "order": 6,
            "visibility": "issue_Type == Cloud backup is failing || issue_Type == Disk backup is failing",
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
            "watermarkText": "Copy and paste error message that you see in console",
            "required": false
        },
        {
            "id": "workload_Type",
            "visibility": "null",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Which type of data source you are backing up?",
            "watermarkText": "Select workload type",
            "dropdownOptions": [
                {
                    "value": "File Server",
                    "text": "File Server"
                },
                {
                    "value": "SQL database",
                    "text": "SQL database"
                },
                {
                    "value": "Exchange Server",
                    "text": "Exchange Server"
                },
                {
                    "value": "SharePoint",
                    "text": "SharePoint"
                },
                {
                    "value": "Hyper-V",
                    "text": "Hyper-V"
                },
                {
                    "value": "VMWare",
                    "text": "VMWare"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 8,
            "visibility": "issue_Type == Cloud backup is failing",
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check Azure Backup server <a href='https://aka.ms/AB-AA4dqdk'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
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
                    "value": "Unsupported files are excluded from backup",
                    "text": "Unsupported files are excluded from backup"
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
            "order": 9,
            "visibility": "issue_Type == Cloud backup is failing",
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 10,
            "visibility": "issue_Type == Cloud backup is failing",
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId:",
            "infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 11,
            "visibility": "null",
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 12,
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
