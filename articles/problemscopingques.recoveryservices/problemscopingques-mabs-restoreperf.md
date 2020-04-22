<properties
         pageTitle="Scoping questions for Azure backup server restore perf"
         description="Scoping questions for Azure backup server restore perf"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612999,32632809"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
  	 articleId="3d0e2537-0802-4def-88da-de618f915950"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure backup server restore performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure backup server restore is taking longer",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure backup server restore is taking longer",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "issue_Type",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the restoration type:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Restore from cloud is slow",
                    "text": "Restore from cloud is slow"
                },
                {
                    "value": "Restore from disk is slow",
                    "text": "Restore from disk is slow"
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
            "id": "mab_version",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "infoBalloonText": "You can find version information from Microsoft Azure Backup Server Console\\Help\\About",
            "displayLabel": "What is the software version of Microsoft Azure Backup Server?",
            "watermarkText": "ex. version 12.0.332.0.",
            "required": false
        },
        {
            "id": "error_message",
            "order": 3,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
            "watermarkText": "Copy and paste error message that you see in console",
            "required": false
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 4,
            "visibility": "issue_Type == Restore from cloud is slow",
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check Azure Backup server restore <a href='https://aka.ms/AA4ev9l'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
                },
                {
                    "value": "Ensured there is sufficient disk space to restore the data",
                    "text": "Ensured there is sufficient disk space to restore the data"
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
            "order": 5,
            "visibility": "issue_Type == Cloud backup is failing",
            "controlType": "textbox",
            "displayLabel": "Provide the MachineId:",
            "infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 6,
            "visibility": "issue_Type == Cloud backup is failing",
            "controlType": "textbox",
            "displayLabel": "Provide the ResourceId:",
            "infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "visibility": "null",
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 8,
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
