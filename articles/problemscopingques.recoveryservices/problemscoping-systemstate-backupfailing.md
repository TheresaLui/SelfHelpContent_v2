<properties
         pageTitle="Scoping questions for system state backup failure"
         description="Scoping questions for system state backup failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32594866"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="fc35ea46-7f1c-43aa-84bd-c85caf7ed73b"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions system state backup failure
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "System State backup failure",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "System State backup failure",
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
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
            "watermarkText": "Copy and paste error message text from failed job details dialog in Microsoft Azure Backup agent",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 5,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check System State backup <a href='https://aka.ms/AB-SystemState-Tshooting'>Troubleshooting</a> article",
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
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "get_machineid",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "You can find the MachineId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId:",
            "infoBalloonText": "You can find the ResourceId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
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
