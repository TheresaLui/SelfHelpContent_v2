<properties
         pageTitle="Scoping questions for MARS restore failure"
         description="Scoping questions for MARS restore failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553296"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="171f4f9b-3e04-4b40-8c57-b30b5063c752"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions MARS restore failure
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "MARS restore failure",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "MARS restore failure",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
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
            "required": false
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text from failed job details dialog in Microsoft Azure Backup agent",
            "required": false
        },
        {
            "id": "get_machineid",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId:",
            "infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "recoverymode_type",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Which type of recovery mode are you performing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Individual files and folders",
                    "text": "Individual files and folders"
                },
                {
                    "value": "Volume",
                    "text": "Volume"
                }
            ],
            "required": false
        },
        {
            "id": "restore_location",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Which type of restoration are you performing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Restore data to an alternate machine",
                    "text": "Restore data to an alternate machine"
                },
                {
                    "value": "Restore data to the same machine from which the backups were taken",
                    "text": "Restore data to the same machine from which the backups were taken"
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
            "id": "basic_troubleshooting_multiselect",
            "order": 8,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "Passphrase used for restore and backup are same",
                    "text": "Passphrase used for restore and backup are same"
                },
                {
                    "value": "If restoring to alternate machine, then the OS version is same/higher than original",
                    "text": "If restoring to alternate machine, then the OS version is same/higher than original"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "Microsoft iSCSI Initiator service is running",
                    "text": "Microsoft iSCSI Initiator service is running"
                },
                {
                    "value": "Tried restoring different recovery points",
                    "text": "Tried restoring different recovery points"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 10,
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
