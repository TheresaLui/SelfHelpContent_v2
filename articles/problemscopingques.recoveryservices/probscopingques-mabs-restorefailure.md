<properties
         pageTitle="Scoping questions for Azure backup server Restore Failure"
         description="Scoping questions for Azure backup server Restore Failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553295"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
		     articleId="92647b9e-7319-47d5-a6c4-1453dfa3e33f"
/>
# Questions Azure backup server - Restore Failure
---
{
    "resourceRequired": true,
    "title": "Azure backup server restore failure",
    "fileAttachmentHint": "",
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
                }
            ],
            "required": true
        },
        {
            "id": "os_version",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the impacted system?",
            "watermarkText": "ex. Windows 2012 R2",
            "required": true
        },
        {
            "id": "machine_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the impacted machine",
            "required": true
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text from the console instead of screenshot",
            "required": true
        },
        {
            "id": "get_machineid",
            "order": 5,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "watermarkText": "Find from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 6,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId",
            "watermarkText": "Find from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
            "required": false
        },
        {
            "id": "restore_location",
            "order": 7,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "dropdown",
            "displayLabel": "Which type of recovery are you performing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Recover data to an alternate location",
                    "text": "Recover data to an alternate location"
                },
                {
                    "value": "Recover data to the original location",
                    "text": "Recover data to the original location"
                }
            ],
            "required": false
        },
        {
            "id": "data_source_type",
            "order": 8,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "dropdown",
            "displayLabel": "Which type of data source are you restoring?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Restoring files and folder",
                    "text": "Restoring files and folder"
                },
                {
                    "value": "Restoring system state backup",
                    "text": "Restoring system state backup"
                },
                {
                    "value": "Restoring Hyper-V or VMWare VMs",
                    "text": "Restoring Hyper-V or VMWare VMs"
                },
                {
                    "value": "Restoring SQL database",
                    "text": "Restoring SQL database"
                },
                {
                    "value": "Restoring Exchange database",
                    "text": "Restoring Exchange database"
                },
                {
                    "value": "Restoring SharePoint farm",
                    "text": "Restoring SharePoint farm"
                }
            ],
            "required": true
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 9,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed:",
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
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_date",
            "order": 10,
            "visibility": "issue_Type == Restore from cloud || issue_Type == Restore from disk",
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "learn_more_text1",
            "order": 11,
            "visibility": "issue_Type == Restore from cloud",
            "controlType": "infoblock",
            "content": "Please upload CBEngine log files located at %ProgramFiles%\\Microsoft Azure Recovery Services Agent\\Temp. Put all the contents to be shared into a single ZIP file and upload the file using 'File upload' on the left."
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
    ]
}
---
