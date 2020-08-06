<properties
         pageTitle="Scoping questions for MARS backup completes with warnings"
         description="Scoping questions for MARS backup completes with warnings"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632793"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="d7bbf0c8-35a5-4759-92d4-4a8640c05585"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for MARS backup completes with warnings
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "MARS backup completes with warnings",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "machine_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the Windows Server or Windows Client",
            "required": true
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
                },
                {
                    "value": "Retried backup operation but backup still failed",
                    "text": "Retried backup operation but backup still failed"
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
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
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
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId:",
            "infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
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
