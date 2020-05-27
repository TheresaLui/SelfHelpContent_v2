<properties
         pageTitle="Scoping questions for MABS scheduled backup is not run automatically"
         description="Scoping questions for MABS scheduled backup is not run automatically"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632805"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="6c1b6a4b-e827-47f6-bfa8-556ae26e6ad8"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions MABS scheduled backup is not run automatically
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "MABS scheduled backup is not run automatically",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "MABS scheduled backup is not run automatically",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "os_version",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the machine where Azure Backup server is installed?",
            "watermarkText": "ex. Windows 2012 R2",
            "required": false
        },
        {
            "id": "machine_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the machine having MABS installed",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 3,
            "controlType": "multiselectdropdown",
	    "infoBalloonText": "Check scheduled backup job failures <a href='https://aka.ms/AB-MABS-ScheduledBackupNotRun'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
                },
                {
                    "value": "Verified the SQL Scheduler is running fine",
                    "text": "Verified the SQL Scheduler is running fine"
                },
                {
                    "value": "Ensured no previous backup job is in progress",
                    "text": "Ensured no previous backup job is in progress"
                },
                {
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
		{
                    "value": "Firewall settings on the machine/proxy are configured to allow the required URLs",
                    "text": "Firewall settings on the machine/proxy are configured to allow the required URLs"
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
			"infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
            "watermarkText": "Paste MachineId here",
            "required": false
        },
        {
            "id": "get_resourceId",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide the ResourceId:",
			"infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
            "watermarkText": "Paste ResourceId here",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
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
