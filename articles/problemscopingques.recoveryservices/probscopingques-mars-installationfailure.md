<properties
         pageTitle="Scoping questions for MARS Installation or registration failure"
         description="Scoping questions for MARS Installation or registration failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553287"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="0d4bc270-b32b-49f9-8b5c-c6d01db47adf"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions MARS Installation or registration failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "MARS Installation or registration failure",
    "fileAttachmentHint": "",
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
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text from failed job details dialog in Microsoft Azure Backup agent",
            "required": false
        },
        {
            "id": "registration_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is this an intial-registration/re-registering issue?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Initial-registration",
                    "text": "Initial-registration"
                },
                {
                    "value": "Re-registering",
                    "text": "Re-registering"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
	{
	 "id": "issue_type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Which type of issue you are facing?",
            "dropdownOptions": [
                {
                    "value": "Proxy Configuration failed",
                    "text": "Proxy Configuration failed"
                },
                {
                    "value": "Installing pre-requisites (.NET and PowerShell) failed",
                    "text": "Installing pre-requisites (.NET and PowerShell) failed"
                },
                {
                    "value": "Issue with Vault Credentials",
                    "text": "Issue with Vault Credentials"
                },
                {
                    "value": "Issue with encryption-key/passphrase",
                    "text": "Issue with encryption-key/passphrase"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
	},
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 6,
            "controlType": "multiselectdropdown",
			"infoBalloonText": "Check installation and registration <a href='https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "OS version is supported for backup",
                    "text": "OS version is supported for backup"
                },
                {
                    "value": "If firewall is used, then required URLs are whitelisted",
                    "text": "If firewall is used, then required URLs are whitelisted"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
                },
                {
                    "value": ".NET framework version is at least 4.6.2",
                    "text": ".NET framework version is at least 4.6.2"
                },
                {
                    "value": "Server is not registered with another vault",
                    "text": "Server is not registered with another vault"
                },
                {
                    "value": "Ensure c:/windows/temp folder has less than 60,000 files",
                    "text": "Ensure c:/windows/temp folder has less than 60,000 files"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
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
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
