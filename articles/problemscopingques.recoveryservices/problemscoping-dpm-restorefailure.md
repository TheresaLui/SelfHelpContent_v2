<properties
         pageTitle="Scoping questions for DPM Restore Failure"
         description="Scoping questions for DPM Restore Failure"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553300"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="a3318b66-8d65-4588-8eeb-4fec45b46791"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions DPM - Restore Failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "DPM restore failure",
    "fileAttachmentHint": "",
     "diagnosticCard": {
        "title": "DPM restore failure",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "issue_Type",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you restoring from disk/cloud?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Restore from cloud",
                    "text": "Restore from cloud"
                },
                {
                    "value": "Restore from disk",
                    "text": "Restore from disk"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "os_version",
            "order": 2,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the impacted system?",
            "watermarkText": "ex. Windows 2012 R2",
            "required": false
        },
        {
            "id": "machine_name",
            "order": 3,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the impacted machine",
            "required": false
        },
        {
            "id": "error_message",
            "order": 4,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "textbox",
            "displayLabel": "Provide the error code that you are seeing:",
            "watermarkText": "Example: DataTransferServiceCoFLimitReached",
            "required": false
        },
        {
            "id": "get_machineid",
            "order": 5,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 6,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId",
            "infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "restore_location",
            "order": 7,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "dropdown",
            "displayLabel": "Which type of recovery you are performing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Recover data to an alternate location",
                    "text": "Recover data to an alternate location"
                },
                {
                    "value": "Recover data to the original location",
                    "text": "Recover data to the original location"
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
            "id": "data_source_type",
            "order": 8,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "dropdown",
            "displayLabel": "Which type of data source you are restoring?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Restoring files and folder",
                    "text": "Restoring files and folder"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 9,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check System Center Data Protection Manager <a href='https://aka.ms/AB-DPM-tshooting'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Passphrase used during restore and backup are same",
                    "text": "Passphrase used during restore and backup are same"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
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
            "order": 10,
            "visibility": "issue_Type == Restore from cloud || issue_Type == Restore from disk",
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 11,
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
