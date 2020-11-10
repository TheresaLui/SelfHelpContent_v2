<properties
         pageTitle="Scoping questions for System State restore failure"
         description="Scoping questions for System State restore failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32594870"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="d82a2f62-74a2-4e0f-9fc3-e81782434a1f"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions System State restore failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "System State restore failing",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "System State restore failing",
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
            "required": true
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
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
            "id": "restore_location",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Which type of recovery you are performing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Recovering System State files to the same server",
                    "text": "Recovering System State files to the same server"
                },
                {
                    "value": "Recovering System State files to an alternate server",
                    "text": "Recovering System State files to an alternate server"
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
            "id": "issue_type",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "At what stage of recovery you are facing issue?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Recovering System State files",
                    "text": "Recovering System State files"
                },
                {
                    "value": "Applying restored System State on a Windows Server",
                    "text": "Applying restored System State on a Windows Server"
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
            "infoBalloonText": "Check System State restore failure <a href='https://aka.ms/AB-AA4dwsp'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
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
                    "value": "If restoring to alternate server, ensured the OS version is same/higher than original",
                    "text": "If restoring to alternate server, ensured the OS version is same/higher than original"
                },
                {
                    "value": "If restoring to alternate server, Ensured both source and target machine are registered with same vault",
                    "text": "If restoring to alternate server, Ensured both source and target machine are registered with same vault"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
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
